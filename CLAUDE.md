popup.js:
```
import {
    s as et,
    a as Fu,
    c as D1
} from "./api-BSAJ5K5U.js";
(function () {
    const b = document.createElement("link").relList;
    if (b && b.supports && b.supports("modulepreload")) return;
    for (const h of document.querySelectorAll('link[rel="modulepreload"]')) o(h);
    new MutationObserver(h => {
        for (const z of h)
            if (z.type === "childList")
                for (const C of z.addedNodes) C.tagName === "LINK" && C.rel === "modulepreload" && o(C)
    }).observe(document, {
        childList: !0,
        subtree: !0
    });

    function N(h) {
        const z = {};
        return h.integrity && (z.integrity = h.integrity), h.referrerPolicy && (z.referrerPolicy = h.referrerPolicy), h.crossOrigin === "use-credentials" ? z.credentials = "include" : h.crossOrigin === "anonymous" ? z.credentials = "omit" : z.credentials = "same-origin", z
    }

    function o(h) {
        if (h.ep) return;
        h.ep = !0;
        const z = N(h);
        fetch(h.href, z)
    }
})();
var bs = {
        exports: {}
    },
    Mn = {};
var qd;

function A1() {
    if (qd) return Mn;
    qd = 1;
    var f = Symbol.for("react.transitional.element"),
        b = Symbol.for("react.fragment");

    function N(o, h, z) {
        var C = null;
        if (z !== void 0 && (C = "" + z), h.key !== void 0 && (C = "" + h.key), "key" in h) {
            z = {};
            for (var R in h) R !== "key" && (z[R] = h[R])
        } else z = h;
        return h = z.ref, {
            $$typeof: f,
            type: o,
            key: C,
            ref: h !== void 0 ? h : null,
            props: z
        }
    }
    return Mn.Fragment = b, Mn.jsx = N, Mn.jsxs = N, Mn
}
var Bd;

function _1() {
    return Bd || (Bd = 1, bs.exports = A1()), bs.exports
}
var c = _1(),
    Ns = {
        exports: {}
    },
    P = {};
var Ld;

function O1() {
    if (Ld) return P;
    Ld = 1;
    var f = Symbol.for("react.transitional.element"),
        b = Symbol.for("react.portal"),
        N = Symbol.for("react.fragment"),
        o = Symbol.for("react.strict_mode"),
        h = Symbol.for("react.profiler"),
        z = Symbol.for("react.consumer"),
        C = Symbol.for("react.context"),
        R = Symbol.for("react.forward_ref"),
        _ = Symbol.for("react.suspense"),
        S = Symbol.for("react.memo"),
        q = Symbol.for("react.lazy"),
        M = Symbol.for("react.activity"),
        X = Symbol.iterator;

    function w(m) {
        return m === null || typeof m != "object" ? null : (m = X && m[X] || m["@@iterator"], typeof m == "function" ? m : null)
    }
    var V = {
            isMounted: function () {
                return !1
            },
            enqueueForceUpdate: function () {},
            enqueueReplaceState: function () {},
            enqueueSetState: function () {}
        },
        K = Object.assign,
        ae = {};

    function J(m, A, B) {
        this.props = m, this.context = A, this.refs = ae, this.updater = B || V
    }
    J.prototype.isReactComponent = {}, J.prototype.setState = function (m, A) {
        if (typeof m != "object" && typeof m != "function" && m != null) throw Error("takes an object of state variables to update or a function which returns an object of state variables.");
        this.updater.enqueueSetState(this, m, A, "setState")
    }, J.prototype.forceUpdate = function (m) {
        this.updater.enqueueForceUpdate(this, m, "forceUpdate")
    };

    function ze() {}
    ze.prototype = J.prototype;

    function F(m, A, B) {
        this.props = m, this.context = A, this.refs = ae, this.updater = B || V
    }
    var Re = F.prototype = new ze;
    Re.constructor = F, K(Re, J.prototype), Re.isPureReactComponent = !0;
    var W = Array.isArray;

    function Q() {}
    var O = {
            H: null,
            A: null,
            T: null,
            S: null
        },
        U = Object.prototype.hasOwnProperty;

    function ne(m, A, B) {
        var Y = B.ref;
        return {
            $$typeof: f,
            type: m,
            key: A,
            ref: Y !== void 0 ? Y : null,
            props: B
        }
    }

    function Ue(m, A) {
        return ne(m.type, A, m.props)
    }

    function je(m) {
        return typeof m == "object" && m !== null && m.$$typeof === f
    }

    function Me(m) {
        var A = {
            "=": "=0",
            ":": "=2"
        };
        return "$" + m.replace(/[=:]/g, function (B) {
            return A[B]
        })
    }
    var Ie = /\/+/g;

    function Ze(m, A) {
        return typeof m == "object" && m !== null && m.key != null ? Me("" + m.key) : A.toString(36)
    }

    function De(m) {
        switch (m.status) {
        case "fulfilled":
            return m.value;
        case "rejected":
            throw m.reason;
        default:
            switch (typeof m.status == "string" ? m.then(Q, Q) : (m.status = "pending", m.then(function (A) {
                m.status === "pending" && (m.status = "fulfilled", m.value = A)
            }, function (A) {
                m.status === "pending" && (m.status = "rejected", m.reason = A)
            })), m.status) {
            case "fulfilled":
                return m.value;
            case "rejected":
                throw m.reason
            }
        }
        throw m
    }

    function x(m, A, B, Y, ee) {
        var ue = typeof m;
        (ue === "undefined" || ue === "boolean") && (m = null);
        var ve = !1;
        if (m === null) ve = !0;
        else switch (ue) {
        case "bigint":
        case "string":
        case "number":
            ve = !0;
            break;
        case "object":
            switch (m.$$typeof) {
            case f:
            case b:
                ve = !0;
                break;
            case q:
                return ve = m._init, x(ve(m._payload), A, B, Y, ee)
            }
        }
        if (ve) return ee = ee(m), ve = Y === "" ? "." + Ze(m, 0) : Y, W(ee) ? (B = "", ve != null && (B = ve.replace(Ie, "$&/") + "/"), x(ee, A, B, "", function (Ua) {
            return Ua
        })) : ee != null && (je(ee) && (ee = Ue(ee, B + (ee.key == null || m && m.key === ee.key ? "" : ("" + ee.key).replace(Ie, "$&/") + "/") + ve)), A.push(ee)), 1;
        ve = 0;
        var tt = Y === "" ? "." : Y + ":";
        if (W(m))
            for (var qe = 0; qe < m.length; qe++) Y = m[qe], ue = tt + Ze(Y, qe), ve += x(Y, A, B, ue, ee);
        else if (qe = w(m), typeof qe == "function")
            for (m = qe.call(m), qe = 0; !(Y = m.next()).done;) Y = Y.value, ue = tt + Ze(Y, qe++), ve += x(Y, A, B, ue, ee);
        else if (ue === "object") {
            if (typeof m.then == "function") return x(De(m), A, B, Y, ee);
            throw A = String(m), Error("Objects are not valid as a React child (found: " + (A === "[object Object]" ? "object with keys {" + Object.keys(m).join(", ") + "}" : A) + "). If you meant to render a collection of children, use an array instead.")
        }
        return ve
    }

    function H(m, A, B) {
        if (m == null) return m;
        var Y = [],
            ee = 0;
        return x(m, Y, "", "", function (ue) {
            return A.call(B, ue, ee++)
        }), Y
    }

    function I(m) {
        if (m._status === -1) {
            var A = m._result;
            A = A(), A.then(function (B) {
                (m._status === 0 || m._status === -1) && (m._status = 1, m._result = B)
            }, function (B) {
                (m._status === 0 || m._status === -1) && (m._status = 2, m._result = B)
            }), m._status === -1 && (m._status = 0, m._result = A)
        }
        if (m._status === 1) return m._result.default;
        throw m._result
    }
    var Se = typeof reportError == "function" ? reportError : function (m) {
            if (typeof window == "object" && typeof window.ErrorEvent == "function") {
                var A = new window.ErrorEvent("error", {
                    bubbles: !0,
                    cancelable: !0,
                    message: typeof m == "object" && m !== null && typeof m.message == "string" ? String(m.message) : String(m),
                    error: m
                });
                if (!window.dispatchEvent(A)) return
            } else if (typeof process == "object" && typeof process.emit == "function") {
                process.emit("uncaughtException", m);
                return
            }
            console.error(m)
        },
        Te = {
            map: H,
            forEach: function (m, A, B) {
                H(m, function () {
                    A.apply(this, arguments)
                }, B)
            },
            count: function (m) {
                var A = 0;
                return H(m, function () {
                    A++
                }), A
            },
            toArray: function (m) {
                return H(m, function (A) {
                    return A
                }) || []
            },
            only: function (m) {
                if (!je(m)) throw Error("React.Children.only expected to receive a single React element child.");
                return m
            }
        };
    return P.Activity = M, P.Children = Te, P.Component = J, P.Fragment = N, P.Profiler = h, P.PureComponent = F, P.StrictMode = o, P.Suspense = _, P.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE = O, P.__COMPILER_RUNTIME = {
        __proto__: null,
        c: function (m) {
            return O.H.useMemoCache(m)
        }
    }, P.cache = function (m) {
        return function () {
            return m.apply(null, arguments)
        }
    }, P.cacheSignal = function () {
        return null
    }, P.cloneElement = function (m, A, B) {
        if (m == null) throw Error("The argument must be a React element, but you passed " + m + ".");
        var Y = K({}, m.props),
            ee = m.key;
        if (A != null)
            for (ue in A.key !== void 0 && (ee = "" + A.key), A) !U.call(A, ue) || ue === "key" || ue === "__self" || ue === "__source" || ue === "ref" && A.ref === void 0 || (Y[ue] = A[ue]);
        var ue = arguments.length - 2;
        if (ue === 1) Y.children = B;
        else if (1 < ue) {
            for (var ve = Array(ue), tt = 0; tt < ue; tt++) ve[tt] = arguments[tt + 2];
            Y.children = ve
        }
        return ne(m.type, ee, Y)
    }, P.createContext = function (m) {
        return m = {
            $$typeof: C,
            _currentValue: m,
            _currentValue2: m,
            _threadCount: 0,
            Provider: null,
            Consumer: null
        }, m.Provider = m, m.Consumer = {
            $$typeof: z,
            _context: m
        }, m
    }, P.createElement = function (m, A, B) {
        var Y, ee = {},
            ue = null;
        if (A != null)
            for (Y in A.key !== void 0 && (ue = "" + A.key), A) U.call(A, Y) && Y !== "key" && Y !== "__self" && Y !== "__source" && (ee[Y] = A[Y]);
        var ve = arguments.length - 2;
        if (ve === 1) ee.children = B;
        else if (1 < ve) {
            for (var tt = Array(ve), qe = 0; qe < ve; qe++) tt[qe] = arguments[qe + 2];
            ee.children = tt
        }
        if (m && m.defaultProps)
            for (Y in ve = m.defaultProps, ve) ee[Y] === void 0 && (ee[Y] = ve[Y]);
        return ne(m, ue, ee)
    }, P.createRef = function () {
        return {
            current: null
        }
    }, P.forwardRef = function (m) {
        return {
            $$typeof: R,
            render: m
        }
    }, P.isValidElement = je, P.lazy = function (m) {
        return {
            $$typeof: q,
            _payload: {
                _status: -1,
                _result: m
            },
            _init: I
        }
    }, P.memo = function (m, A) {
        return {
            $$typeof: S,
            type: m,
            compare: A === void 0 ? null : A
        }
    }, P.startTransition = function (m) {
        var A = O.T,
            B = {};
        O.T = B;
        try {
            var Y = m(),
                ee = O.S;
            ee !== null && ee(B, Y), typeof Y == "object" && Y !== null && typeof Y.then == "function" && Y.then(Q, Se)
        } catch (ue) {
            Se(ue)
        } finally {
            A !== null && B.types !== null && (A.types = B.types), O.T = A
        }
    }, P.unstable_useCacheRefresh = function () {
        return O.H.useCacheRefresh()
    }, P.use = function (m) {
        return O.H.use(m)
    }, P.useActionState = function (m, A, B) {
        return O.H.useActionState(m, A, B)
    }, P.useCallback = function (m, A) {
        return O.H.useCallback(m, A)
    }, P.useContext = function (m) {
        return O.H.useContext(m)
    }, P.useDebugValue = function () {}, P.useDeferredValue = function (m, A) {
        return O.H.useDeferredValue(m, A)
    }, P.useEffect = function (m, A) {
        return O.H.useEffect(m, A)
    }, P.useEffectEvent = function (m) {
        return O.H.useEffectEvent(m)
    }, P.useId = function () {
        return O.H.useId()
    }, P.useImperativeHandle = function (m, A, B) {
        return O.H.useImperativeHandle(m, A, B)
    }, P.useInsertionEffect = function (m, A) {
        return O.H.useInsertionEffect(m, A)
    }, P.useLayoutEffect = function (m, A) {
        return O.H.useLayoutEffect(m, A)
    }, P.useMemo = function (m, A) {
        return O.H.useMemo(m, A)
    }, P.useOptimistic = function (m, A) {
        return O.H.useOptimistic(m, A)
    }, P.useReducer = function (m, A, B) {
        return O.H.useReducer(m, A, B)
    }, P.useRef = function (m) {
        return O.H.useRef(m)
    }, P.useState = function (m) {
        return O.H.useState(m)
    }, P.useSyncExternalStore = function (m, A, B) {
        return O.H.useSyncExternalStore(m, A, B)
    }, P.useTransition = function () {
        return O.H.useTransition()
    }, P.version = "19.2.3", P
}
var kd;

function _s() {
    return kd || (kd = 1, Ns.exports = O1()), Ns.exports
}
var L = _s(),
    Es = {
        exports: {}
    },
    Dn = {},
    Ts = {
        exports: {}
    },
    xs = {};
var Yd;

function R1() {
    return Yd || (Yd = 1, (function (f) {
        function b(x, H) {
            var I = x.length;
            x.push(H);
            e: for (; 0 < I;) {
                var Se = I - 1 >>> 1,
                    Te = x[Se];
                if (0 < h(Te, H)) x[Se] = H, x[I] = Te, I = Se;
                else break e
            }
        }

        function N(x) {
            return x.length === 0 ? null : x[0]
        }

        function o(x) {
            if (x.length === 0) return null;
            var H = x[0],
                I = x.pop();
            if (I !== H) {
                x[0] = I;
                e: for (var Se = 0, Te = x.length, m = Te >>> 1; Se < m;) {
                    var A = 2 * (Se + 1) - 1,
                        B = x[A],
                        Y = A + 1,
                        ee = x[Y];
                    if (0 > h(B, I)) Y < Te && 0 > h(ee, B) ? (x[Se] = ee, x[Y] = I, Se = Y) : (x[Se] = B, x[A] = I, Se = A);
                    else if (Y < Te && 0 > h(ee, I)) x[Se] = ee, x[Y] = I, Se = Y;
                    else break e
                }
            }
            return H
        }

        function h(x, H) {
            var I = x.sortIndex - H.sortIndex;
            return I !== 0 ? I : x.id - H.id
        }
        if (f.unstable_now = void 0, typeof performance == "object" && typeof performance.now == "function") {
            var z = performance;
            f.unstable_now = function () {
                return z.now()
            }
        } else {
            var C = Date,
                R = C.now();
            f.unstable_now = function () {
                return C.now() - R
            }
        }
        var _ = [],
            S = [],
            q = 1,
            M = null,
            X = 3,
            w = !1,
            V = !1,
            K = !1,
            ae = !1,
            J = typeof setTimeout == "function" ? setTimeout : null,
            ze = typeof clearTimeout == "function" ? clearTimeout : null,
            F = typeof setImmediate < "u" ? setImmediate : null;

        function Re(x) {
            for (var H = N(S); H !== null;) {
                if (H.callback === null) o(S);
                else if (H.startTime <= x) o(S), H.sortIndex = H.expirationTime, b(_, H);
                else break;
                H = N(S)
            }
        }

        function W(x) {
            if (K = !1, Re(x), !V)
                if (N(_) !== null) V = !0, Q || (Q = !0, Me());
                else {
                    var H = N(S);
                    H !== null && De(W, H.startTime - x)
                }
        }
        var Q = !1,
            O = -1,
            U = 5,
            ne = -1;

        function Ue() {
            return ae ? !0 : !(f.unstable_now() - ne < U)
        }

        function je() {
            if (ae = !1, Q) {
                var x = f.unstable_now();
                ne = x;
                var H = !0;
                try {
                    e: {
                        V = !1,
                        K && (K = !1, ze(O), O = -1),
                        w = !0;
                        var I = X;
                        try {
                            t: {
                                for (Re(x), M = N(_); M !== null && !(M.expirationTime > x && Ue());) {
                                    var Se = M.callback;
                                    if (typeof Se == "function") {
                                        M.callback = null, X = M.priorityLevel;
                                        var Te = Se(M.expirationTime <= x);
                                        if (x = f.unstable_now(), typeof Te == "function") {
                                            M.callback = Te, Re(x), H = !0;
                                            break t
                                        }
                                        M === N(_) && o(_), Re(x)
                                    } else o(_);
                                    M = N(_)
                                }
                                if (M !== null) H = !0;
                                else {
                                    var m = N(S);
                                    m !== null && De(W, m.startTime - x), H = !1
                                }
                            }
                            break e
                        }
                        finally {
                            M = null, X = I, w = !1
                        }
                        H = void 0
                    }
                }
                finally {
                    H ? Me() : Q = !1
                }
            }
        }
        var Me;
        if (typeof F == "function") Me = function () {
            F(je)
        };
        else if (typeof MessageChannel < "u") {
            var Ie = new MessageChannel,
                Ze = Ie.port2;
            Ie.port1.onmessage = je, Me = function () {
                Ze.postMessage(null)
            }
        } else Me = function () {
            J(je, 0)
        };

        function De(x, H) {
            O = J(function () {
                x(f.unstable_now())
            }, H)
        }
        f.unstable_IdlePriority = 5, f.unstable_ImmediatePriority = 1, f.unstable_LowPriority = 4, f.unstable_NormalPriority = 3, f.unstable_Profiling = null, f.unstable_UserBlockingPriority = 2, f.unstable_cancelCallback = function (x) {
            x.callback = null
        }, f.unstable_forceFrameRate = function (x) {
            0 > x || 125 < x ? console.error("forceFrameRate takes a positive int between 0 and 125, forcing frame rates higher than 125 fps is not supported") : U = 0 < x ? Math.floor(1e3 / x) : 5
        }, f.unstable_getCurrentPriorityLevel = function () {
            return X
        }, f.unstable_next = function (x) {
            switch (X) {
            case 1:
            case 2:
            case 3:
                var H = 3;
                break;
            default:
                H = X
            }
            var I = X;
            X = H;
            try {
                return x()
            } finally {
                X = I
            }
        }, f.unstable_requestPaint = function () {
            ae = !0
        }, f.unstable_runWithPriority = function (x, H) {
            switch (x) {
            case 1:
            case 2:
            case 3:
            case 4:
            case 5:
                break;
            default:
                x = 3
            }
            var I = X;
            X = x;
            try {
                return H()
            } finally {
                X = I
            }
        }, f.unstable_scheduleCallback = function (x, H, I) {
            var Se = f.unstable_now();
            switch (typeof I == "object" && I !== null ? (I = I.delay, I = typeof I == "number" && 0 < I ? Se + I : Se) : I = Se, x) {
            case 1:
                var Te = -1;
                break;
            case 2:
                Te = 250;
                break;
            case 5:
                Te = 1073741823;
                break;
            case 4:
                Te = 1e4;
                break;
            default:
                Te = 5e3
            }
            return Te = I + Te, x = {
                id: q++,
                callback: H,
                priorityLevel: x,
                startTime: I,
                expirationTime: Te,
                sortIndex: -1
            }, I > Se ? (x.sortIndex = I, b(S, x), N(_) === null && x === N(S) && (K ? (ze(O), O = -1) : K = !0, De(W, I - Se))) : (x.sortIndex = Te, b(_, x), V || w || (V = !0, Q || (Q = !0, Me()))), x
        }, f.unstable_shouldYield = Ue, f.unstable_wrapCallback = function (x) {
            var H = X;
            return function () {
                var I = X;
                X = H;
                try {
                    return x.apply(this, arguments)
                } finally {
                    X = I
                }
            }
        }
    })(xs)), xs
}
var Gd;

function U1() {
    return Gd || (Gd = 1, Ts.exports = R1()), Ts.exports
}
var zs = {
        exports: {}
    },
    Pe = {};
var Xd;

function C1() {
    if (Xd) return Pe;
    Xd = 1;
    var f = _s();

    function b(_) {
        var S = "https://react.dev/errors/" + _;
        if (1 < arguments.length) {
            S += "?args[]=" + encodeURIComponent(arguments[1]);
            for (var q = 2; q < arguments.length; q++) S += "&args[]=" + encodeURIComponent(arguments[q])
        }
        return "Minified React error #" + _ + "; visit " + S + " for the full message or use the non-minified dev environment for full errors and additional helpful warnings."
    }

    function N() {}
    var o = {
            d: {
                f: N,
                r: function () {
                    throw Error(b(522))
                },
                D: N,
                C: N,
                L: N,
                m: N,
                X: N,
                S: N,
                M: N
            },
            p: 0,
            findDOMNode: null
        },
        h = Symbol.for("react.portal");

    function z(_, S, q) {
        var M = 3 < arguments.length && arguments[3] !== void 0 ? arguments[3] : null;
        return {
            $$typeof: h,
            key: M == null ? null : "" + M,
            children: _,
            containerInfo: S,
            implementation: q
        }
    }
    var C = f.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE;

    function R(_, S) {
        if (_ === "font") return "";
        if (typeof S == "string") return S === "use-credentials" ? S : ""
    }
    return Pe.__DOM_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE = o, Pe.createPortal = function (_, S) {
        var q = 2 < arguments.length && arguments[2] !== void 0 ? arguments[2] : null;
        if (!S || S.nodeType !== 1 && S.nodeType !== 9 && S.nodeType !== 11) throw Error(b(299));
        return z(_, S, null, q)
    }, Pe.flushSync = function (_) {
        var S = C.T,
            q = o.p;
        try {
            if (C.T = null, o.p = 2, _) return _()
        } finally {
            C.T = S, o.p = q, o.d.f()
        }
    }, Pe.preconnect = function (_, S) {
        typeof _ == "string" && (S ? (S = S.crossOrigin, S = typeof S == "string" ? S === "use-credentials" ? S : "" : void 0) : S = null, o.d.C(_, S))
    }, Pe.prefetchDNS = function (_) {
        typeof _ == "string" && o.d.D(_)
    }, Pe.preinit = function (_, S) {
        if (typeof _ == "string" && S && typeof S.as == "string") {
            var q = S.as,
                M = R(q, S.crossOrigin),
                X = typeof S.integrity == "string" ? S.integrity : void 0,
                w = typeof S.fetchPriority == "string" ? S.fetchPriority : void 0;
            q === "style" ? o.d.S(_, typeof S.precedence == "string" ? S.precedence : void 0, {
                crossOrigin: M,
                integrity: X,
                fetchPriority: w
            }) : q === "script" && o.d.X(_, {
                crossOrigin: M,
                integrity: X,
                fetchPriority: w,
                nonce: typeof S.nonce == "string" ? S.nonce : void 0
            })
        }
    }, Pe.preinitModule = function (_, S) {
        if (typeof _ == "string")
            if (typeof S == "object" && S !== null) {
                if (S.as == null || S.as === "script") {
                    var q = R(S.as, S.crossOrigin);
                    o.d.M(_, {
                        crossOrigin: q,
                        integrity: typeof S.integrity == "string" ? S.integrity : void 0,
                        nonce: typeof S.nonce == "string" ? S.nonce : void 0
                    })
                }
            } else S == null && o.d.M(_)
    }, Pe.preload = function (_, S) {
        if (typeof _ == "string" && typeof S == "object" && S !== null && typeof S.as == "string") {
            var q = S.as,
                M = R(q, S.crossOrigin);
            o.d.L(_, q, {
                crossOrigin: M,
                integrity: typeof S.integrity == "string" ? S.integrity : void 0,
                nonce: typeof S.nonce == "string" ? S.nonce : void 0,
                type: typeof S.type == "string" ? S.type : void 0,
                fetchPriority: typeof S.fetchPriority == "string" ? S.fetchPriority : void 0,
                referrerPolicy: typeof S.referrerPolicy == "string" ? S.referrerPolicy : void 0,
                imageSrcSet: typeof S.imageSrcSet == "string" ? S.imageSrcSet : void 0,
                imageSizes: typeof S.imageSizes == "string" ? S.imageSizes : void 0,
                media: typeof S.media == "string" ? S.media : void 0
            })
        }
    }, Pe.preloadModule = function (_, S) {
        if (typeof _ == "string")
            if (S) {
                var q = R(S.as, S.crossOrigin);
                o.d.m(_, {
                    as: typeof S.as == "string" && S.as !== "script" ? S.as : void 0,
                    crossOrigin: q,
                    integrity: typeof S.integrity == "string" ? S.integrity : void 0
                })
            } else o.d.m(_)
    }, Pe.requestFormReset = function (_) {
        o.d.r(_)
    }, Pe.unstable_batchedUpdates = function (_, S) {
        return _(S)
    }, Pe.useFormState = function (_, S, q) {
        return C.H.useFormState(_, S, q)
    }, Pe.useFormStatus = function () {
        return C.H.useHostTransitionStatus()
    }, Pe.version = "19.2.3", Pe
}
var Qd;

function H1() {
    if (Qd) return zs.exports;
    Qd = 1;

    function f() {
        if (!(typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ > "u" || typeof __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE != "function")) try {
            __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE(f)
        } catch (b) {
            console.error(b)
        }
    }
    return f(), zs.exports = C1(), zs.exports
}
var Vd;

function q1() {
    if (Vd) return Dn;
    Vd = 1;
    var f = U1(),
        b = _s(),
        N = H1();

    function o(e) {
        var t = "https://react.dev/errors/" + e;
        if (1 < arguments.length) {
            t += "?args[]=" + encodeURIComponent(arguments[1]);
            for (var l = 2; l < arguments.length; l++) t += "&args[]=" + encodeURIComponent(arguments[l])
        }
        return "Minified React error #" + e + "; visit " + t + " for the full message or use the non-minified dev environment for full errors and additional helpful warnings."
    }

    function h(e) {
        return !(!e || e.nodeType !== 1 && e.nodeType !== 9 && e.nodeType !== 11)
    }

    function z(e) {
        var t = e,
            l = e;
        if (e.alternate)
            for (; t.return;) t = t.return;
        else {
            e = t;
            do t = e, (t.flags & 4098) !== 0 && (l = t.return), e = t.return; while (e)
        }
        return t.tag === 3 ? l : null
    }

    function C(e) {
        if (e.tag === 13) {
            var t = e.memoizedState;
            if (t === null && (e = e.alternate, e !== null && (t = e.memoizedState)), t !== null) return t.dehydrated
        }
        return null
    }

    function R(e) {
        if (e.tag === 31) {
            var t = e.memoizedState;
            if (t === null && (e = e.alternate, e !== null && (t = e.memoizedState)), t !== null) return t.dehydrated
        }
        return null
    }

    function _(e) {
        if (z(e) !== e) throw Error(o(188))
    }

    function S(e) {
        var t = e.alternate;
        if (!t) {
            if (t = z(e), t === null) throw Error(o(188));
            return t !== e ? null : e
        }
        for (var l = e, a = t;;) {
            var n = l.return;
            if (n === null) break;
            var u = n.alternate;
            if (u === null) {
                if (a = n.return, a !== null) {
                    l = a;
                    continue
                }
                break
            }
            if (n.child === u.child) {
                for (u = n.child; u;) {
                    if (u === l) return _(n), e;
                    if (u === a) return _(n), t;
                    u = u.sibling
                }
                throw Error(o(188))
            }
            if (l.return !== a.return) l = n, a = u;
            else {
                for (var i = !1, s = n.child; s;) {
                    if (s === l) {
                        i = !0, l = n, a = u;
                        break
                    }
                    if (s === a) {
                        i = !0, a = n, l = u;
                        break
                    }
                    s = s.sibling
                }
                if (!i) {
                    for (s = u.child; s;) {
                        if (s === l) {
                            i = !0, l = u, a = n;
                            break
                        }
                        if (s === a) {
                            i = !0, a = u, l = n;
                            break
                        }
                        s = s.sibling
                    }
                    if (!i) throw Error(o(189))
                }
            }
            if (l.alternate !== a) throw Error(o(190))
        }
        if (l.tag !== 3) throw Error(o(188));
        return l.stateNode.current === l ? e : t
    }

    function q(e) {
        var t = e.tag;
        if (t === 5 || t === 26 || t === 27 || t === 6) return e;
        for (e = e.child; e !== null;) {
            if (t = q(e), t !== null) return t;
            e = e.sibling
        }
        return null
    }
    var M = Object.assign,
        X = Symbol.for("react.element"),
        w = Symbol.for("react.transitional.element"),
        V = Symbol.for("react.portal"),
        K = Symbol.for("react.fragment"),
        ae = Symbol.for("react.strict_mode"),
        J = Symbol.for("react.profiler"),
        ze = Symbol.for("react.consumer"),
        F = Symbol.for("react.context"),
        Re = Symbol.for("react.forward_ref"),
        W = Symbol.for("react.suspense"),
        Q = Symbol.for("react.suspense_list"),
        O = Symbol.for("react.memo"),
        U = Symbol.for("react.lazy"),
        ne = Symbol.for("react.activity"),
        Ue = Symbol.for("react.memo_cache_sentinel"),
        je = Symbol.iterator;

    function Me(e) {
        return e === null || typeof e != "object" ? null : (e = je && e[je] || e["@@iterator"], typeof e == "function" ? e : null)
    }
    var Ie = Symbol.for("react.client.reference");

    function Ze(e) {
        if (e == null) return null;
        if (typeof e == "function") return e.$$typeof === Ie ? null : e.displayName || e.name || null;
        if (typeof e == "string") return e;
        switch (e) {
        case K:
            return "Fragment";
        case J:
            return "Profiler";
        case ae:
            return "StrictMode";
        case W:
            return "Suspense";
        case Q:
            return "SuspenseList";
        case ne:
            return "Activity"
        }
        if (typeof e == "object") switch (e.$$typeof) {
        case V:
            return "Portal";
        case F:
            return e.displayName || "Context";
        case ze:
            return (e._context.displayName || "Context") + ".Consumer";
        case Re:
            var t = e.render;
            return e = e.displayName, e || (e = t.displayName || t.name || "", e = e !== "" ? "ForwardRef(" + e + ")" : "ForwardRef"), e;
        case O:
            return t = e.displayName || null, t !== null ? t : Ze(e.type) || "Memo";
        case U:
            t = e._payload, e = e._init;
            try {
                return Ze(e(t))
            } catch {}
        }
        return null
    }
    var De = Array.isArray,
        x = b.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE,
        H = N.__DOM_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE,
        I = {
            pending: !1,
            data: null,
            method: null,
            action: null
        },
        Se = [],
        Te = -1;

    function m(e) {
        return {
            current: e
        }
    }

    function A(e) {
        0 > Te || (e.current = Se[Te], Se[Te] = null, Te--)
    }

    function B(e, t) {
        Te++, Se[Te] = e.current, e.current = t
    }
    var Y = m(null),
        ee = m(null),
        ue = m(null),
        ve = m(null);

    function tt(e, t) {
        switch (B(ue, t), B(ee, e), B(Y, null), t.nodeType) {
        case 9:
        case 11:
            e = (e = t.documentElement) && (e = e.namespaceURI) ? ud(e) : 0;
            break;
        default:
            if (e = t.tagName, t = t.namespaceURI) t = ud(t), e = id(t, e);
            else switch (e) {
            case "svg":
                e = 1;
                break;
            case "math":
                e = 2;
                break;
            default:
                e = 0
            }
        }
        A(Y), B(Y, e)
    }

    function qe() {
        A(Y), A(ee), A(ue)
    }

    function Ua(e) {
        e.memoizedState !== null && B(ve, e);
        var t = Y.current,
            l = id(t, e.type);
        t !== l && (B(ee, e), B(Y, l))
    }

    function On(e) {
        ee.current === e && (A(Y), A(ee)), ve.current === e && (A(ve), Tn._currentValue = I)
    }
    var li, Us;

    function Dl(e) {
        if (li === void 0) try {
            throw Error()
        } catch (l) {
            var t = l.stack.trim().match(/\n( *(at )?)/);
            li = t && t[1] || "", Us = -1 < l.stack.indexOf(`
    at`) ? " (<anonymous>)" : -1 < l.stack.indexOf("@") ? "@unknown:0:0" : ""
        }
        return `
` + li + e + Us
    }
    var ai = !1;

    function ni(e, t) {
        if (!e || ai) return "";
        ai = !0;
        var l = Error.prepareStackTrace;
        Error.prepareStackTrace = void 0;
        try {
            var a = {
                DetermineComponentFrameRoot: function () {
                    try {
                        if (t) {
                            var D = function () {
                                throw Error()
                            };
                            if (Object.defineProperty(D.prototype, "props", {
                                    set: function () {
                                        throw Error()
                                    }
                                }), typeof Reflect == "object" && Reflect.construct) {
                                try {
                                    Reflect.construct(D, [])
                                } catch (E) {
                                    var p = E
                                }
                                Reflect.construct(e, [], D)
                            } else {
                                try {
                                    D.call()
                                } catch (E) {
                                    p = E
                                }
                                e.call(D.prototype)
                            }
                        } else {
                            try {
                                throw Error()
                            } catch (E) {
                                p = E
                            }(D = e()) && typeof D.catch == "function" && D.catch(function () {})
                        }
                    } catch (E) {
                        if (E && p && typeof E.stack == "string") return [E.stack, p.stack]
                    }
                    return [null, null]
                }
            };
            a.DetermineComponentFrameRoot.displayName = "DetermineComponentFrameRoot";
            var n = Object.getOwnPropertyDescriptor(a.DetermineComponentFrameRoot, "name");
            n && n.configurable && Object.defineProperty(a.DetermineComponentFrameRoot, "name", {
                value: "DetermineComponentFrameRoot"
            });
            var u = a.DetermineComponentFrameRoot(),
                i = u[0],
                s = u[1];
            if (i && s) {
                var r = i.split(`
`),
                    y = s.split(`
`);
                for (n = a = 0; a < r.length && !r[a].includes("DetermineComponentFrameRoot");) a++;
                for (; n < y.length && !y[n].includes("DetermineComponentFrameRoot");) n++;
                if (a === r.length || n === y.length)
                    for (a = r.length - 1, n = y.length - 1; 1 <= a && 0 <= n && r[a] !== y[n];) n--;
                for (; 1 <= a && 0 <= n; a--, n--)
                    if (r[a] !== y[n]) {
                        if (a !== 1 || n !== 1)
                            do
                                if (a--, n--, 0 > n || r[a] !== y[n]) {
                                    var T = `
` + r[a].replace(" at new ", " at ");
                                    return e.displayName && T.includes("<anonymous>") && (T = T.replace("<anonymous>", e.displayName)), T
                                } while (1 <= a && 0 <= n);
                        break
                    }
            }
        } finally {
            ai = !1, Error.prepareStackTrace = l
        }
        return (l = e ? e.displayName || e.name : "") ? Dl(l) : ""
    }

    function um(e, t) {
        switch (e.tag) {
        case 26:
        case 27:
        case 5:
            return Dl(e.type);
        case 16:
            return Dl("Lazy");
        case 13:
            return e.child !== t && t !== null ? Dl("Suspense Fallback") : Dl("Suspense");
        case 19:
            return Dl("SuspenseList");
        case 0:
        case 15:
            return ni(e.type, !1);
        case 11:
            return ni(e.type.render, !1);
        case 1:
            return ni(e.type, !0);
        case 31:
            return Dl("Activity");
        default:
            return ""
        }
    }

    function Cs(e) {
        try {
            var t = "",
                l = null;
            do t += um(e, l), l = e, e = e.return; while (e);
            return t
        } catch (a) {
            return `
Error generating stack: ` + a.message + `
` + a.stack
        }
    }
    var ui = Object.prototype.hasOwnProperty,
        ii = f.unstable_scheduleCallback,
        ci = f.unstable_cancelCallback,
        im = f.unstable_shouldYield,
        cm = f.unstable_requestPaint,
        rt = f.unstable_now,
        sm = f.unstable_getCurrentPriorityLevel,
        Hs = f.unstable_ImmediatePriority,
        qs = f.unstable_UserBlockingPriority,
        Rn = f.unstable_NormalPriority,
        fm = f.unstable_LowPriority,
        Bs = f.unstable_IdlePriority,
        om = f.log,
        rm = f.unstable_setDisableYieldValue,
        Ca = null,
        dt = null;

    function al(e) {
        if (typeof om == "function" && rm(e), dt && typeof dt.setStrictMode == "function") try {
            dt.setStrictMode(Ca, e)
        } catch {}
    }
    var mt = Math.clz32 ? Math.clz32 : hm,
        dm = Math.log,
        mm = Math.LN2;

    function hm(e) {
        return e >>>= 0, e === 0 ? 32 : 31 - (dm(e) / mm | 0) | 0
    }
    var Un = 256,
        Cn = 262144,
        Hn = 4194304;

    function Al(e) {
        var t = e & 42;
        if (t !== 0) return t;
        switch (e & -e) {
        case 1:
            return 1;
        case 2:
            return 2;
        case 4:
            return 4;
        case 8:
            return 8;
        case 16:
            return 16;
        case 32:
            return 32;
        case 64:
            return 64;
        case 128:
            return 128;
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
            return e & 261888;
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
            return e & 3932160;
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
            return e & 62914560;
        case 67108864:
            return 67108864;
        case 134217728:
            return 134217728;
        case 268435456:
            return 268435456;
        case 536870912:
            return 536870912;
        case 1073741824:
            return 0;
        default:
            return e
        }
    }

    function qn(e, t, l) {
        var a = e.pendingLanes;
        if (a === 0) return 0;
        var n = 0,
            u = e.suspendedLanes,
            i = e.pingedLanes;
        e = e.warmLanes;
        var s = a & 134217727;
        return s !== 0 ? (a = s & ~u, a !== 0 ? n = Al(a) : (i &= s, i !== 0 ? n = Al(i) : l || (l = s & ~e, l !== 0 && (n = Al(l))))) : (s = a & ~u, s !== 0 ? n = Al(s) : i !== 0 ? n = Al(i) : l || (l = a & ~e, l !== 0 && (n = Al(l)))), n === 0 ? 0 : t !== 0 && t !== n && (t & u) === 0 && (u = n & -n, l = t & -t, u >= l || u === 32 && (l & 4194048) !== 0) ? t : n
    }

    function Ha(e, t) {
        return (e.pendingLanes & ~(e.suspendedLanes & ~e.pingedLanes) & t) === 0
    }

    function vm(e, t) {
        switch (e) {
        case 1:
        case 2:
        case 4:
        case 8:
        case 64:
            return t + 250;
        case 16:
        case 32:
        case 128:
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
            return t + 5e3;
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
            return -1;
        case 67108864:
        case 134217728:
        case 268435456:
        case 536870912:
        case 1073741824:
            return -1;
        default:
            return -1
        }
    }

    function Ls() {
        var e = Hn;
        return Hn <<= 1, (Hn & 62914560) === 0 && (Hn = 4194304), e
    }

    function si(e) {
        for (var t = [], l = 0; 31 > l; l++) t.push(e);
        return t
    }

    function qa(e, t) {
        e.pendingLanes |= t, t !== 268435456 && (e.suspendedLanes = 0, e.pingedLanes = 0, e.warmLanes = 0)
    }

    function gm(e, t, l, a, n, u) {
        var i = e.pendingLanes;
        e.pendingLanes = l, e.suspendedLanes = 0, e.pingedLanes = 0, e.warmLanes = 0, e.expiredLanes &= l, e.entangledLanes &= l, e.errorRecoveryDisabledLanes &= l, e.shellSuspendCounter = 0;
        var s = e.entanglements,
            r = e.expirationTimes,
            y = e.hiddenUpdates;
        for (l = i & ~l; 0 < l;) {
            var T = 31 - mt(l),
                D = 1 << T;
            s[T] = 0, r[T] = -1;
            var p = y[T];
            if (p !== null)
                for (y[T] = null, T = 0; T < p.length; T++) {
                    var E = p[T];
                    E !== null && (E.lane &= -536870913)
                }
            l &= ~D
        }
        a !== 0 && ks(e, a, 0), u !== 0 && n === 0 && e.tag !== 0 && (e.suspendedLanes |= u & ~(i & ~t))
    }

    function ks(e, t, l) {
        e.pendingLanes |= t, e.suspendedLanes &= ~t;
        var a = 31 - mt(t);
        e.entangledLanes |= t, e.entanglements[a] = e.entanglements[a] | 1073741824 | l & 261930
    }

    function Ys(e, t) {
        var l = e.entangledLanes |= t;
        for (e = e.entanglements; l;) {
            var a = 31 - mt(l),
                n = 1 << a;
            n & t | e[a] & t && (e[a] |= t), l &= ~n
        }
    }

    function Gs(e, t) {
        var l = t & -t;
        return l = (l & 42) !== 0 ? 1 : fi(l), (l & (e.suspendedLanes | t)) !== 0 ? 0 : l
    }

    function fi(e) {
        switch (e) {
        case 2:
            e = 1;
            break;
        case 8:
            e = 4;
            break;
        case 32:
            e = 16;
            break;
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
            e = 128;
            break;
        case 268435456:
            e = 134217728;
            break;
        default:
            e = 0
        }
        return e
    }

    function oi(e) {
        return e &= -e, 2 < e ? 8 < e ? (e & 134217727) !== 0 ? 32 : 268435456 : 8 : 2
    }

    function Xs() {
        var e = H.p;
        return e !== 0 ? e : (e = window.event, e === void 0 ? 32 : Ad(e.type))
    }

    function Qs(e, t) {
        var l = H.p;
        try {
            return H.p = e, t()
        } finally {
            H.p = l
        }
    }
    var nl = Math.random().toString(36).slice(2),
        Ke = "__reactFiber$" + nl,
        at = "__reactProps$" + nl,
        Kl = "__reactContainer$" + nl,
        ri = "__reactEvents$" + nl,
        ym = "__reactListeners$" + nl,
        pm = "__reactHandles$" + nl,
        Vs = "__reactResources$" + nl,
        Ba = "__reactMarker$" + nl;

    function di(e) {
        delete e[Ke], delete e[at], delete e[ri], delete e[ym], delete e[pm]
    }

    function Jl(e) {
        var t = e[Ke];
        if (t) return t;
        for (var l = e.parentNode; l;) {
            if (t = l[Kl] || l[Ke]) {
                if (l = t.alternate, t.child !== null || l !== null && l.child !== null)
                    for (e = md(e); e !== null;) {
                        if (l = e[Ke]) return l;
                        e = md(e)
                    }
                return t
            }
            e = l, l = e.parentNode
        }
        return null
    }

    function Wl(e) {
        if (e = e[Ke] || e[Kl]) {
            var t = e.tag;
            if (t === 5 || t === 6 || t === 13 || t === 31 || t === 26 || t === 27 || t === 3) return e
        }
        return null
    }

    function La(e) {
        var t = e.tag;
        if (t === 5 || t === 26 || t === 27 || t === 6) return e.stateNode;
        throw Error(o(33))
    }

    function $l(e) {
        var t = e[Vs];
        return t || (t = e[Vs] = {
            hoistableStyles: new Map,
            hoistableScripts: new Map
        }), t
    }

    function Ve(e) {
        e[Ba] = !0
    }
    var ws = new Set,
        Zs = {};

    function _l(e, t) {
        Fl(e, t), Fl(e + "Capture", t)
    }

    function Fl(e, t) {
        for (Zs[e] = t, e = 0; e < t.length; e++) ws.add(t[e])
    }
    var Sm = RegExp("^[:A-Z_a-z\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02FF\\u0370-\\u037D\\u037F-\\u1FFF\\u200C-\\u200D\\u2070-\\u218F\\u2C00-\\u2FEF\\u3001-\\uD7FF\\uF900-\\uFDCF\\uFDF0-\\uFFFD][:A-Z_a-z\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02FF\\u0370-\\u037D\\u037F-\\u1FFF\\u200C-\\u200D\\u2070-\\u218F\\u2C00-\\u2FEF\\u3001-\\uD7FF\\uF900-\\uFDCF\\uFDF0-\\uFFFD\\-.0-9\\u00B7\\u0300-\\u036F\\u203F-\\u2040]*$"),
        Ks = {},
        Js = {};

    function bm(e) {
        return ui.call(Js, e) ? !0 : ui.call(Ks, e) ? !1 : Sm.test(e) ? Js[e] = !0 : (Ks[e] = !0, !1)
    }

    function Bn(e, t, l) {
        if (bm(t))
            if (l === null) e.removeAttribute(t);
            else {
                switch (typeof l) {
                case "undefined":
                case "function":
                case "symbol":
                    e.removeAttribute(t);
                    return;
                case "boolean":
                    var a = t.toLowerCase().slice(0, 5);
                    if (a !== "data-" && a !== "aria-") {
                        e.removeAttribute(t);
                        return
                    }
                }
                e.setAttribute(t, "" + l)
            }
    }

    function Ln(e, t, l) {
        if (l === null) e.removeAttribute(t);
        else {
            switch (typeof l) {
            case "undefined":
            case "function":
            case "symbol":
            case "boolean":
                e.removeAttribute(t);
                return
            }
            e.setAttribute(t, "" + l)
        }
    }

    function kt(e, t, l, a) {
        if (a === null) e.removeAttribute(l);
        else {
            switch (typeof a) {
            case "undefined":
            case "function":
            case "symbol":
            case "boolean":
                e.removeAttribute(l);
                return
            }
            e.setAttributeNS(t, l, "" + a)
        }
    }

    function Nt(e) {
        switch (typeof e) {
        case "bigint":
        case "boolean":
        case "number":
        case "string":
        case "undefined":
            return e;
        case "object":
            return e;
        default:
            return ""
        }
    }

    function Ws(e) {
        var t = e.type;
        return (e = e.nodeName) && e.toLowerCase() === "input" && (t === "checkbox" || t === "radio")
    }

    function Nm(e, t, l) {
        var a = Object.getOwnPropertyDescriptor(e.constructor.prototype, t);
        if (!e.hasOwnProperty(t) && typeof a < "u" && typeof a.get == "function" && typeof a.set == "function") {
            var n = a.get,
                u = a.set;
            return Object.defineProperty(e, t, {
                configurable: !0,
                get: function () {
                    return n.call(this)
                },
                set: function (i) {
                    l = "" + i, u.call(this, i)
                }
            }), Object.defineProperty(e, t, {
                enumerable: a.enumerable
            }), {
                getValue: function () {
                    return l
                },
                setValue: function (i) {
                    l = "" + i
                },
                stopTracking: function () {
                    e._valueTracker = null, delete e[t]
                }
            }
        }
    }

    function mi(e) {
        if (!e._valueTracker) {
            var t = Ws(e) ? "checked" : "value";
            e._valueTracker = Nm(e, t, "" + e[t])
        }
    }

    function $s(e) {
        if (!e) return !1;
        var t = e._valueTracker;
        if (!t) return !0;
        var l = t.getValue(),
            a = "";
        return e && (a = Ws(e) ? e.checked ? "true" : "false" : e.value), e = a, e !== l ? (t.setValue(e), !0) : !1
    }

    function kn(e) {
        if (e = e || (typeof document < "u" ? document : void 0), typeof e > "u") return null;
        try {
            return e.activeElement || e.body
        } catch {
            return e.body
        }
    }
    var Em = /[\n"\\]/g;

    function Et(e) {
        return e.replace(Em, function (t) {
            return "\\" + t.charCodeAt(0).toString(16) + " "
        })
    }

    function hi(e, t, l, a, n, u, i, s) {
        e.name = "", i != null && typeof i != "function" && typeof i != "symbol" && typeof i != "boolean" ? e.type = i : e.removeAttribute("type"), t != null ? i === "number" ? (t === 0 && e.value === "" || e.value != t) && (e.value = "" + Nt(t)) : e.value !== "" + Nt(t) && (e.value = "" + Nt(t)) : i !== "submit" && i !== "reset" || e.removeAttribute("value"), t != null ? vi(e, i, Nt(t)) : l != null ? vi(e, i, Nt(l)) : a != null && e.removeAttribute("value"), n == null && u != null && (e.defaultChecked = !!u), n != null && (e.checked = n && typeof n != "function" && typeof n != "symbol"), s != null && typeof s != "function" && typeof s != "symbol" && typeof s != "boolean" ? e.name = "" + Nt(s) : e.removeAttribute("name")
    }

    function Fs(e, t, l, a, n, u, i, s) {
        if (u != null && typeof u != "function" && typeof u != "symbol" && typeof u != "boolean" && (e.type = u), t != null || l != null) {
            if (!(u !== "submit" && u !== "reset" || t != null)) {
                mi(e);
                return
            }
            l = l != null ? "" + Nt(l) : "", t = t != null ? "" + Nt(t) : l, s || t === e.value || (e.value = t), e.defaultValue = t
        }
        a = a ?? n, a = typeof a != "function" && typeof a != "symbol" && !!a, e.checked = s ? e.checked : !!a, e.defaultChecked = !!a, i != null && typeof i != "function" && typeof i != "symbol" && typeof i != "boolean" && (e.name = i), mi(e)
    }

    function vi(e, t, l) {
        t === "number" && kn(e.ownerDocument) === e || e.defaultValue === "" + l || (e.defaultValue = "" + l)
    }

    function Il(e, t, l, a) {
        if (e = e.options, t) {
            t = {};
            for (var n = 0; n < l.length; n++) t["$" + l[n]] = !0;
            for (l = 0; l < e.length; l++) n = t.hasOwnProperty("$" + e[l].value), e[l].selected !== n && (e[l].selected = n), n && a && (e[l].defaultSelected = !0)
        } else {
            for (l = "" + Nt(l), t = null, n = 0; n < e.length; n++) {
                if (e[n].value === l) {
                    e[n].selected = !0, a && (e[n].defaultSelected = !0);
                    return
                }
                t !== null || e[n].disabled || (t = e[n])
            }
            t !== null && (t.selected = !0)
        }
    }

    function Is(e, t, l) {
        if (t != null && (t = "" + Nt(t), t !== e.value && (e.value = t), l == null)) {
            e.defaultValue !== t && (e.defaultValue = t);
            return
        }
        e.defaultValue = l != null ? "" + Nt(l) : ""
    }

    function Ps(e, t, l, a) {
        if (t == null) {
            if (a != null) {
                if (l != null) throw Error(o(92));
                if (De(a)) {
                    if (1 < a.length) throw Error(o(93));
                    a = a[0]
                }
                l = a
            }
            l == null && (l = ""), t = l
        }
        l = Nt(t), e.defaultValue = l, a = e.textContent, a === l && a !== "" && a !== null && (e.value = a), mi(e)
    }

    function Pl(e, t) {
        if (t) {
            var l = e.firstChild;
            if (l && l === e.lastChild && l.nodeType === 3) {
                l.nodeValue = t;
                return
            }
        }
        e.textContent = t
    }
    var Tm = new Set("animationIterationCount aspectRatio borderImageOutset borderImageSlice borderImageWidth boxFlex boxFlexGroup boxOrdinalGroup columnCount columns flex flexGrow flexPositive flexShrink flexNegative flexOrder gridArea gridRow gridRowEnd gridRowSpan gridRowStart gridColumn gridColumnEnd gridColumnSpan gridColumnStart fontWeight lineClamp lineHeight opacity order orphans scale tabSize widows zIndex zoom fillOpacity floodOpacity stopOpacity strokeDasharray strokeDashoffset strokeMiterlimit strokeOpacity strokeWidth MozAnimationIterationCount MozBoxFlex MozBoxFlexGroup MozLineClamp msAnimationIterationCount msFlex msZoom msFlexGrow msFlexNegative msFlexOrder msFlexPositive msFlexShrink msGridColumn msGridColumnSpan msGridRow msGridRowSpan WebkitAnimationIterationCount WebkitBoxFlex WebKitBoxFlexGroup WebkitBoxOrdinalGroup WebkitColumnCount WebkitColumns WebkitFlex WebkitFlexGrow WebkitFlexPositive WebkitFlexShrink WebkitLineClamp".split(" "));

    function ef(e, t, l) {
        var a = t.indexOf("--") === 0;
        l == null || typeof l == "boolean" || l === "" ? a ? e.setProperty(t, "") : t === "float" ? e.cssFloat = "" : e[t] = "" : a ? e.setProperty(t, l) : typeof l != "number" || l === 0 || Tm.has(t) ? t === "float" ? e.cssFloat = l : e[t] = ("" + l).trim() : e[t] = l + "px"
    }

    function tf(e, t, l) {
        if (t != null && typeof t != "object") throw Error(o(62));
        if (e = e.style, l != null) {
            for (var a in l) !l.hasOwnProperty(a) || t != null && t.hasOwnProperty(a) || (a.indexOf("--") === 0 ? e.setProperty(a, "") : a === "float" ? e.cssFloat = "" : e[a] = "");
            for (var n in t) a = t[n], t.hasOwnProperty(n) && l[n] !== a && ef(e, n, a)
        } else
            for (var u in t) t.hasOwnProperty(u) && ef(e, u, t[u])
    }

    function gi(e) {
        if (e.indexOf("-") === -1) return !1;
        switch (e) {
        case "annotation-xml":
        case "color-profile":
        case "font-face":
        case "font-face-src":
        case "font-face-uri":
        case "font-face-format":
        case "font-face-name":
        case "missing-glyph":
            return !1;
        default:
            return !0
        }
    }
    var xm = new Map([
            ["acceptCharset", "accept-charset"],
            ["htmlFor", "for"],
            ["httpEquiv", "http-equiv"],
            ["crossOrigin", "crossorigin"],
            ["accentHeight", "accent-height"],
            ["alignmentBaseline", "alignment-baseline"],
            ["arabicForm", "arabic-form"],
            ["baselineShift", "baseline-shift"],
            ["capHeight", "cap-height"],
            ["clipPath", "clip-path"],
            ["clipRule", "clip-rule"],
            ["colorInterpolation", "color-interpolation"],
            ["colorInterpolationFilters", "color-interpolation-filters"],
            ["colorProfile", "color-profile"],
            ["colorRendering", "color-rendering"],
            ["dominantBaseline", "dominant-baseline"],
            ["enableBackground", "enable-background"],
            ["fillOpacity", "fill-opacity"],
            ["fillRule", "fill-rule"],
            ["floodColor", "flood-color"],
            ["floodOpacity", "flood-opacity"],
            ["fontFamily", "font-family"],
            ["fontSize", "font-size"],
            ["fontSizeAdjust", "font-size-adjust"],
            ["fontStretch", "font-stretch"],
            ["fontStyle", "font-style"],
            ["fontVariant", "font-variant"],
            ["fontWeight", "font-weight"],
            ["glyphName", "glyph-name"],
            ["glyphOrientationHorizontal", "glyph-orientation-horizontal"],
            ["glyphOrientationVertical", "glyph-orientation-vertical"],
            ["horizAdvX", "horiz-adv-x"],
            ["horizOriginX", "horiz-origin-x"],
            ["imageRendering", "image-rendering"],
            ["letterSpacing", "letter-spacing"],
            ["lightingColor", "lighting-color"],
            ["markerEnd", "marker-end"],
            ["markerMid", "marker-mid"],
            ["markerStart", "marker-start"],
            ["overlinePosition", "overline-position"],
            ["overlineThickness", "overline-thickness"],
            ["paintOrder", "paint-order"],
            ["panose-1", "panose-1"],
            ["pointerEvents", "pointer-events"],
            ["renderingIntent", "rendering-intent"],
            ["shapeRendering", "shape-rendering"],
            ["stopColor", "stop-color"],
            ["stopOpacity", "stop-opacity"],
            ["strikethroughPosition", "strikethrough-position"],
            ["strikethroughThickness", "strikethrough-thickness"],
            ["strokeDasharray", "stroke-dasharray"],
            ["strokeDashoffset", "stroke-dashoffset"],
            ["strokeLinecap", "stroke-linecap"],
            ["strokeLinejoin", "stroke-linejoin"],
            ["strokeMiterlimit", "stroke-miterlimit"],
            ["strokeOpacity", "stroke-opacity"],
            ["strokeWidth", "stroke-width"],
            ["textAnchor", "text-anchor"],
            ["textDecoration", "text-decoration"],
            ["textRendering", "text-rendering"],
            ["transformOrigin", "transform-origin"],
            ["underlinePosition", "underline-position"],
            ["underlineThickness", "underline-thickness"],
            ["unicodeBidi", "unicode-bidi"],
            ["unicodeRange", "unicode-range"],
            ["unitsPerEm", "units-per-em"],
            ["vAlphabetic", "v-alphabetic"],
            ["vHanging", "v-hanging"],
            ["vIdeographic", "v-ideographic"],
            ["vMathematical", "v-mathematical"],
            ["vectorEffect", "vector-effect"],
            ["vertAdvY", "vert-adv-y"],
            ["vertOriginX", "vert-origin-x"],
            ["vertOriginY", "vert-origin-y"],
            ["wordSpacing", "word-spacing"],
            ["writingMode", "writing-mode"],
            ["xmlnsXlink", "xmlns:xlink"],
            ["xHeight", "x-height"]
        ]),
        zm = /^[\u0000-\u001F ]*j[\r\n\t]*a[\r\n\t]*v[\r\n\t]*a[\r\n\t]*s[\r\n\t]*c[\r\n\t]*r[\r\n\t]*i[\r\n\t]*p[\r\n\t]*t[\r\n\t]*:/i;

    function Yn(e) {
        return zm.test("" + e) ? "javascript:throw new Error('React has blocked a javascript: URL as a security precaution.')" : e
    }

    function Yt() {}
    var yi = null;

    function pi(e) {
        return e = e.target || e.srcElement || window, e.correspondingUseElement && (e = e.correspondingUseElement), e.nodeType === 3 ? e.parentNode : e
    }
    var ea = null,
        ta = null;

    function lf(e) {
        var t = Wl(e);
        if (t && (e = t.stateNode)) {
            var l = e[at] || null;
            e: switch (e = t.stateNode, t.type) {
            case "input":
                if (hi(e, l.value, l.defaultValue, l.defaultValue, l.checked, l.defaultChecked, l.type, l.name), t = l.name, l.type === "radio" && t != null) {
                    for (l = e; l.parentNode;) l = l.parentNode;
                    for (l = l.querySelectorAll('input[name="' + Et("" + t) + '"][type="radio"]'), t = 0; t < l.length; t++) {
                        var a = l[t];
                        if (a !== e && a.form === e.form) {
                            var n = a[at] || null;
                            if (!n) throw Error(o(90));
                            hi(a, n.value, n.defaultValue, n.defaultValue, n.checked, n.defaultChecked, n.type, n.name)
                        }
                    }
                    for (t = 0; t < l.length; t++) a = l[t], a.form === e.form && $s(a)
                }
                break e;
            case "textarea":
                Is(e, l.value, l.defaultValue);
                break e;
            case "select":
                t = l.value, t != null && Il(e, !!l.multiple, t, !1)
            }
        }
    }
    var Si = !1;

    function af(e, t, l) {
        if (Si) return e(t, l);
        Si = !0;
        try {
            var a = e(t);
            return a
        } finally {
            if (Si = !1, (ea !== null || ta !== null) && (Mu(), ea && (t = ea, e = ta, ta = ea = null, lf(t), e)))
                for (t = 0; t < e.length; t++) lf(e[t])
        }
    }

    function ka(e, t) {
        var l = e.stateNode;
        if (l === null) return null;
        var a = l[at] || null;
        if (a === null) return null;
        l = a[t];
        e: switch (t) {
        case "onClick":
        case "onClickCapture":
        case "onDoubleClick":
        case "onDoubleClickCapture":
        case "onMouseDown":
        case "onMouseDownCapture":
        case "onMouseMove":
        case "onMouseMoveCapture":
        case "onMouseUp":
        case "onMouseUpCapture":
        case "onMouseEnter":
            (a = !a.disabled) || (e = e.type, a = !(e === "button" || e === "input" || e === "select" || e === "textarea")), e = !a;
            break e;
        default:
            e = !1
        }
        if (e) return null;
        if (l && typeof l != "function") throw Error(o(231, t, typeof l));
        return l
    }
    var Gt = !(typeof window > "u" || typeof window.document > "u" || typeof window.document.createElement > "u"),
        bi = !1;
    if (Gt) try {
        var Ya = {};
        Object.defineProperty(Ya, "passive", {
            get: function () {
                bi = !0
            }
        }), window.addEventListener("test", Ya, Ya), window.removeEventListener("test", Ya, Ya)
    } catch {
        bi = !1
    }
    var ul = null,
        Ni = null,
        Gn = null;

    function nf() {
        if (Gn) return Gn;
        var e, t = Ni,
            l = t.length,
            a, n = "value" in ul ? ul.value : ul.textContent,
            u = n.length;
        for (e = 0; e < l && t[e] === n[e]; e++);
        var i = l - e;
        for (a = 1; a <= i && t[l - a] === n[u - a]; a++);
        return Gn = n.slice(e, 1 < a ? 1 - a : void 0)
    }

    function Xn(e) {
        var t = e.keyCode;
        return "charCode" in e ? (e = e.charCode, e === 0 && t === 13 && (e = 13)) : e = t, e === 10 && (e = 13), 32 <= e || e === 13 ? e : 0
    }

    function Qn() {
        return !0
    }

    function uf() {
        return !1
    }

    function nt(e) {
        function t(l, a, n, u, i) {
            this._reactName = l, this._targetInst = n, this.type = a, this.nativeEvent = u, this.target = i, this.currentTarget = null;
            for (var s in e) e.hasOwnProperty(s) && (l = e[s], this[s] = l ? l(u) : u[s]);
            return this.isDefaultPrevented = (u.defaultPrevented != null ? u.defaultPrevented : u.returnValue === !1) ? Qn : uf, this.isPropagationStopped = uf, this
        }
        return M(t.prototype, {
            preventDefault: function () {
                this.defaultPrevented = !0;
                var l = this.nativeEvent;
                l && (l.preventDefault ? l.preventDefault() : typeof l.returnValue != "unknown" && (l.returnValue = !1), this.isDefaultPrevented = Qn)
            },
            stopPropagation: function () {
                var l = this.nativeEvent;
                l && (l.stopPropagation ? l.stopPropagation() : typeof l.cancelBubble != "unknown" && (l.cancelBubble = !0), this.isPropagationStopped = Qn)
            },
            persist: function () {},
            isPersistent: Qn
        }), t
    }
    var Ol = {
            eventPhase: 0,
            bubbles: 0,
            cancelable: 0,
            timeStamp: function (e) {
                return e.timeStamp || Date.now()
            },
            defaultPrevented: 0,
            isTrusted: 0
        },
        Vn = nt(Ol),
        Ga = M({}, Ol, {
            view: 0,
            detail: 0
        }),
        jm = nt(Ga),
        Ei, Ti, Xa, wn = M({}, Ga, {
            screenX: 0,
            screenY: 0,
            clientX: 0,
            clientY: 0,
            pageX: 0,
            pageY: 0,
            ctrlKey: 0,
            shiftKey: 0,
            altKey: 0,
            metaKey: 0,
            getModifierState: zi,
            button: 0,
            buttons: 0,
            relatedTarget: function (e) {
                return e.relatedTarget === void 0 ? e.fromElement === e.srcElement ? e.toElement : e.fromElement : e.relatedTarget
            },
            movementX: function (e) {
                return "movementX" in e ? e.movementX : (e !== Xa && (Xa && e.type === "mousemove" ? (Ei = e.screenX - Xa.screenX, Ti = e.screenY - Xa.screenY) : Ti = Ei = 0, Xa = e), Ei)
            },
            movementY: function (e) {
                return "movementY" in e ? e.movementY : Ti
            }
        }),
        cf = nt(wn),
        Mm = M({}, wn, {
            dataTransfer: 0
        }),
        Dm = nt(Mm),
        Am = M({}, Ga, {
            relatedTarget: 0
        }),
        xi = nt(Am),
        _m = M({}, Ol, {
            animationName: 0,
            elapsedTime: 0,
            pseudoElement: 0
        }),
        Om = nt(_m),
        Rm = M({}, Ol, {
            clipboardData: function (e) {
                return "clipboardData" in e ? e.clipboardData : window.clipboardData
            }
        }),
        Um = nt(Rm),
        Cm = M({}, Ol, {
            data: 0
        }),
        sf = nt(Cm),
        Hm = {
            Esc: "Escape",
            Spacebar: " ",
            Left: "ArrowLeft",
            Up: "ArrowUp",
            Right: "ArrowRight",
            Down: "ArrowDown",
            Del: "Delete",
            Win: "OS",
            Menu: "ContextMenu",
            Apps: "ContextMenu",
            Scroll: "ScrollLock",
            MozPrintableKey: "Unidentified"
        },
        qm = {
            8: "Backspace",
            9: "Tab",
            12: "Clear",
            13: "Enter",
            16: "Shift",
            17: "Control",
            18: "Alt",
            19: "Pause",
            20: "CapsLock",
            27: "Escape",
            32: " ",
            33: "PageUp",
            34: "PageDown",
            35: "End",
            36: "Home",
            37: "ArrowLeft",
            38: "ArrowUp",
            39: "ArrowRight",
            40: "ArrowDown",
            45: "Insert",
            46: "Delete",
            112: "F1",
            113: "F2",
            114: "F3",
            115: "F4",
            116: "F5",
            117: "F6",
            118: "F7",
            119: "F8",
            120: "F9",
            121: "F10",
            122: "F11",
            123: "F12",
            144: "NumLock",
            145: "ScrollLock",
            224: "Meta"
        },
        Bm = {
            Alt: "altKey",
            Control: "ctrlKey",
            Meta: "metaKey",
            Shift: "shiftKey"
        };

    function Lm(e) {
        var t = this.nativeEvent;
        return t.getModifierState ? t.getModifierState(e) : (e = Bm[e]) ? !!t[e] : !1
    }

    function zi() {
        return Lm
    }
    var km = M({}, Ga, {
            key: function (e) {
                if (e.key) {
                    var t = Hm[e.key] || e.key;
                    if (t !== "Unidentified") return t
                }
                return e.type === "keypress" ? (e = Xn(e), e === 13 ? "Enter" : String.fromCharCode(e)) : e.type === "keydown" || e.type === "keyup" ? qm[e.keyCode] || "Unidentified" : ""
            },
            code: 0,
            location: 0,
            ctrlKey: 0,
            shiftKey: 0,
            altKey: 0,
            metaKey: 0,
            repeat: 0,
            locale: 0,
            getModifierState: zi,
            charCode: function (e) {
                return e.type === "keypress" ? Xn(e) : 0
            },
            keyCode: function (e) {
                return e.type === "keydown" || e.type === "keyup" ? e.keyCode : 0
            },
            which: function (e) {
                return e.type === "keypress" ? Xn(e) : e.type === "keydown" || e.type === "keyup" ? e.keyCode : 0
            }
        }),
        Ym = nt(km),
        Gm = M({}, wn, {
            pointerId: 0,
            width: 0,
            height: 0,
            pressure: 0,
            tangentialPressure: 0,
            tiltX: 0,
            tiltY: 0,
            twist: 0,
            pointerType: 0,
            isPrimary: 0
        }),
        ff = nt(Gm),
        Xm = M({}, Ga, {
            touches: 0,
            targetTouches: 0,
            changedTouches: 0,
            altKey: 0,
            metaKey: 0,
            ctrlKey: 0,
            shiftKey: 0,
            getModifierState: zi
        }),
        Qm = nt(Xm),
        Vm = M({}, Ol, {
            propertyName: 0,
            elapsedTime: 0,
            pseudoElement: 0
        }),
        wm = nt(Vm),
        Zm = M({}, wn, {
            deltaX: function (e) {
                return "deltaX" in e ? e.deltaX : "wheelDeltaX" in e ? -e.wheelDeltaX : 0
            },
            deltaY: function (e) {
                return "deltaY" in e ? e.deltaY : "wheelDeltaY" in e ? -e.wheelDeltaY : "wheelDelta" in e ? -e.wheelDelta : 0
            },
            deltaZ: 0,
            deltaMode: 0
        }),
        Km = nt(Zm),
        Jm = M({}, Ol, {
            newState: 0,
            oldState: 0
        }),
        Wm = nt(Jm),
        $m = [9, 13, 27, 32],
        ji = Gt && "CompositionEvent" in window,
        Qa = null;
    Gt && "documentMode" in document && (Qa = document.documentMode);
    var Fm = Gt && "TextEvent" in window && !Qa,
        of = Gt && (!ji || Qa && 8 < Qa && 11 >= Qa),
        rf = " ",
        df = !1;

    function mf(e, t) {
        switch (e) {
        case "keyup":
            return $m.indexOf(t.keyCode) !== -1;
        case "keydown":
            return t.keyCode !== 229;
        case "keypress":
        case "mousedown":
        case "focusout":
            return !0;
        default:
            return !1
        }
    }

    function hf(e) {
        return e = e.detail, typeof e == "object" && "data" in e ? e.data : null
    }
    var la = !1;

    function Im(e, t) {
        switch (e) {
        case "compositionend":
            return hf(t);
        case "keypress":
            return t.which !== 32 ? null : (df = !0, rf);
        case "textInput":
            return e = t.data, e === rf && df ? null : e;
        default:
            return null
        }
    }

    function Pm(e, t) {
        if (la) return e === "compositionend" || !ji && mf(e, t) ? (e = nf(), Gn = Ni = ul = null, la = !1, e) : null;
        switch (e) {
        case "paste":
            return null;
        case "keypress":
            if (!(t.ctrlKey || t.altKey || t.metaKey) || t.ctrlKey && t.altKey) {
                if (t.char && 1 < t.char.length) return t.char;
                if (t.which) return String.fromCharCode(t.which)
            }
            return null;
        case "compositionend":
            return of && t.locale !== "ko" ? null : t.data;
        default:
            return null
        }
    }
    var eh = {
        color: !0,
        date: !0,
        datetime: !0,
        "datetime-local": !0,
        email: !0,
        month: !0,
        number: !0,
        password: !0,
        range: !0,
        search: !0,
        tel: !0,
        text: !0,
        time: !0,
        url: !0,
        week: !0
    };

    function vf(e) {
        var t = e && e.nodeName && e.nodeName.toLowerCase();
        return t === "input" ? !!eh[e.type] : t === "textarea"
    }

    function gf(e, t, l, a) {
        ea ? ta ? ta.push(a) : ta = [a] : ea = a, t = Cu(t, "onChange"), 0 < t.length && (l = new Vn("onChange", "change", null, l, a), e.push({
            event: l,
            listeners: t
        }))
    }
    var Va = null,
        wa = null;

    function th(e) {
        Pr(e, 0)
    }

    function Zn(e) {
        var t = La(e);
        if ($s(t)) return e
    }

    function yf(e, t) {
        if (e === "change") return t
    }
    var pf = !1;
    if (Gt) {
        var Mi;
        if (Gt) {
            var Di = "oninput" in document;
            if (!Di) {
                var Sf = document.createElement("div");
                Sf.setAttribute("oninput", "return;"), Di = typeof Sf.oninput == "function"
            }
            Mi = Di
        } else Mi = !1;
        pf = Mi && (!document.documentMode || 9 < document.documentMode)
    }

    function bf() {
        Va && (Va.detachEvent("onpropertychange", Nf), wa = Va = null)
    }

    function Nf(e) {
        if (e.propertyName === "value" && Zn(wa)) {
            var t = [];
            gf(t, wa, e, pi(e)), af(th, t)
        }
    }

    function lh(e, t, l) {
        e === "focusin" ? (bf(), Va = t, wa = l, Va.attachEvent("onpropertychange", Nf)) : e === "focusout" && bf()
    }

    function ah(e) {
        if (e === "selectionchange" || e === "keyup" || e === "keydown") return Zn(wa)
    }

    function nh(e, t) {
        if (e === "click") return Zn(t)
    }

    function uh(e, t) {
        if (e === "input" || e === "change") return Zn(t)
    }

    function ih(e, t) {
        return e === t && (e !== 0 || 1 / e === 1 / t) || e !== e && t !== t
    }
    var ht = typeof Object.is == "function" ? Object.is : ih;

    function Za(e, t) {
        if (ht(e, t)) return !0;
        if (typeof e != "object" || e === null || typeof t != "object" || t === null) return !1;
        var l = Object.keys(e),
            a = Object.keys(t);
        if (l.length !== a.length) return !1;
        for (a = 0; a < l.length; a++) {
            var n = l[a];
            if (!ui.call(t, n) || !ht(e[n], t[n])) return !1
        }
        return !0
    }

    function Ef(e) {
        for (; e && e.firstChild;) e = e.firstChild;
        return e
    }

    function Tf(e, t) {
        var l = Ef(e);
        e = 0;
        for (var a; l;) {
            if (l.nodeType === 3) {
                if (a = e + l.textContent.length, e <= t && a >= t) return {
                    node: l,
                    offset: t - e
                };
                e = a
            }
            e: {
                for (; l;) {
                    if (l.nextSibling) {
                        l = l.nextSibling;
                        break e
                    }
                    l = l.parentNode
                }
                l = void 0
            }
            l = Ef(l)
        }
    }

    function xf(e, t) {
        return e && t ? e === t ? !0 : e && e.nodeType === 3 ? !1 : t && t.nodeType === 3 ? xf(e, t.parentNode) : "contains" in e ? e.contains(t) : e.compareDocumentPosition ? !!(e.compareDocumentPosition(t) & 16) : !1 : !1
    }

    function zf(e) {
        e = e != null && e.ownerDocument != null && e.ownerDocument.defaultView != null ? e.ownerDocument.defaultView : window;
        for (var t = kn(e.document); t instanceof e.HTMLIFrameElement;) {
            try {
                var l = typeof t.contentWindow.location.href == "string"
            } catch {
                l = !1
            }
            if (l) e = t.contentWindow;
            else break;
            t = kn(e.document)
        }
        return t
    }

    function Ai(e) {
        var t = e && e.nodeName && e.nodeName.toLowerCase();
        return t && (t === "input" && (e.type === "text" || e.type === "search" || e.type === "tel" || e.type === "url" || e.type === "password") || t === "textarea" || e.contentEditable === "true")
    }
    var ch = Gt && "documentMode" in document && 11 >= document.documentMode,
        aa = null,
        _i = null,
        Ka = null,
        Oi = !1;

    function jf(e, t, l) {
        var a = l.window === l ? l.document : l.nodeType === 9 ? l : l.ownerDocument;
        Oi || aa == null || aa !== kn(a) || (a = aa, "selectionStart" in a && Ai(a) ? a = {
            start: a.selectionStart,
            end: a.selectionEnd
        } : (a = (a.ownerDocument && a.ownerDocument.defaultView || window).getSelection(), a = {
            anchorNode: a.anchorNode,
            anchorOffset: a.anchorOffset,
            focusNode: a.focusNode,
            focusOffset: a.focusOffset
        }), Ka && Za(Ka, a) || (Ka = a, a = Cu(_i, "onSelect"), 0 < a.length && (t = new Vn("onSelect", "select", null, t, l), e.push({
            event: t,
            listeners: a
        }), t.target = aa)))
    }

    function Rl(e, t) {
        var l = {};
        return l[e.toLowerCase()] = t.toLowerCase(), l["Webkit" + e] = "webkit" + t, l["Moz" + e] = "moz" + t, l
    }
    var na = {
            animationend: Rl("Animation", "AnimationEnd"),
            animationiteration: Rl("Animation", "AnimationIteration"),
            animationstart: Rl("Animation", "AnimationStart"),
            transitionrun: Rl("Transition", "TransitionRun"),
            transitionstart: Rl("Transition", "TransitionStart"),
            transitioncancel: Rl("Transition", "TransitionCancel"),
            transitionend: Rl("Transition", "TransitionEnd")
        },
        Ri = {},
        Mf = {};
    Gt && (Mf = document.createElement("div").style, "AnimationEvent" in window || (delete na.animationend.animation, delete na.animationiteration.animation, delete na.animationstart.animation), "TransitionEvent" in window || delete na.transitionend.transition);

    function Ul(e) {
        if (Ri[e]) return Ri[e];
        if (!na[e]) return e;
        var t = na[e],
            l;
        for (l in t)
            if (t.hasOwnProperty(l) && l in Mf) return Ri[e] = t[l];
        return e
    }
    var Df = Ul("animationend"),
        Af = Ul("animationiteration"),
        _f = Ul("animationstart"),
        sh = Ul("transitionrun"),
        fh = Ul("transitionstart"),
        oh = Ul("transitioncancel"),
        Of = Ul("transitionend"),
        Rf = new Map,
        Ui = "abort auxClick beforeToggle cancel canPlay canPlayThrough click close contextMenu copy cut drag dragEnd dragEnter dragExit dragLeave dragOver dragStart drop durationChange emptied encrypted ended error gotPointerCapture input invalid keyDown keyPress keyUp load loadedData loadedMetadata loadStart lostPointerCapture mouseDown mouseMove mouseOut mouseOver mouseUp paste pause play playing pointerCancel pointerDown pointerMove pointerOut pointerOver pointerUp progress rateChange reset resize seeked seeking stalled submit suspend timeUpdate touchCancel touchEnd touchStart volumeChange scroll toggle touchMove waiting wheel".split(" ");
    Ui.push("scrollEnd");

    function Ot(e, t) {
        Rf.set(e, t), _l(t, [e])
    }
    var Kn = typeof reportError == "function" ? reportError : function (e) {
            if (typeof window == "object" && typeof window.ErrorEvent == "function") {
                var t = new window.ErrorEvent("error", {
                    bubbles: !0,
                    cancelable: !0,
                    message: typeof e == "object" && e !== null && typeof e.message == "string" ? String(e.message) : String(e),
                    error: e
                });
                if (!window.dispatchEvent(t)) return
            } else if (typeof process == "object" && typeof process.emit == "function") {
                process.emit("uncaughtException", e);
                return
            }
            console.error(e)
        },
        Tt = [],
        ua = 0,
        Ci = 0;

    function Jn() {
        for (var e = ua, t = Ci = ua = 0; t < e;) {
            var l = Tt[t];
            Tt[t++] = null;
            var a = Tt[t];
            Tt[t++] = null;
            var n = Tt[t];
            Tt[t++] = null;
            var u = Tt[t];
            if (Tt[t++] = null, a !== null && n !== null) {
                var i = a.pending;
                i === null ? n.next = n : (n.next = i.next, i.next = n), a.pending = n
            }
            u !== 0 && Uf(l, n, u)
        }
    }

    function Wn(e, t, l, a) {
        Tt[ua++] = e, Tt[ua++] = t, Tt[ua++] = l, Tt[ua++] = a, Ci |= a, e.lanes |= a, e = e.alternate, e !== null && (e.lanes |= a)
    }

    function Hi(e, t, l, a) {
        return Wn(e, t, l, a), $n(e)
    }

    function Cl(e, t) {
        return Wn(e, null, null, t), $n(e)
    }

    function Uf(e, t, l) {
        e.lanes |= l;
        var a = e.alternate;
        a !== null && (a.lanes |= l);
        for (var n = !1, u = e.return; u !== null;) u.childLanes |= l, a = u.alternate, a !== null && (a.childLanes |= l), u.tag === 22 && (e = u.stateNode, e === null || e._visibility & 1 || (n = !0)), e = u, u = u.return;
        return e.tag === 3 ? (u = e.stateNode, n && t !== null && (n = 31 - mt(l), e = u.hiddenUpdates, a = e[n], a === null ? e[n] = [t] : a.push(t), t.lane = l | 536870912), u) : null
    }

    function $n(e) {
        if (50 < gn) throw gn = 0, Vc = null, Error(o(185));
        for (var t = e.return; t !== null;) e = t, t = e.return;
        return e.tag === 3 ? e.stateNode : null
    }
    var ia = {};

    function rh(e, t, l, a) {
        this.tag = e, this.key = l, this.sibling = this.child = this.return = this.stateNode = this.type = this.elementType = null, this.index = 0, this.refCleanup = this.ref = null, this.pendingProps = t, this.dependencies = this.memoizedState = this.updateQueue = this.memoizedProps = null, this.mode = a, this.subtreeFlags = this.flags = 0, this.deletions = null, this.childLanes = this.lanes = 0, this.alternate = null
    }

    function vt(e, t, l, a) {
        return new rh(e, t, l, a)
    }

    function qi(e) {
        return e = e.prototype, !(!e || !e.isReactComponent)
    }

    function Xt(e, t) {
        var l = e.alternate;
        return l === null ? (l = vt(e.tag, t, e.key, e.mode), l.elementType = e.elementType, l.type = e.type, l.stateNode = e.stateNode, l.alternate = e, e.alternate = l) : (l.pendingProps = t, l.type = e.type, l.flags = 0, l.subtreeFlags = 0, l.deletions = null), l.flags = e.flags & 65011712, l.childLanes = e.childLanes, l.lanes = e.lanes, l.child = e.child, l.memoizedProps = e.memoizedProps, l.memoizedState = e.memoizedState, l.updateQueue = e.updateQueue, t = e.dependencies, l.dependencies = t === null ? null : {
            lanes: t.lanes,
            firstContext: t.firstContext
        }, l.sibling = e.sibling, l.index = e.index, l.ref = e.ref, l.refCleanup = e.refCleanup, l
    }

    function Cf(e, t) {
        e.flags &= 65011714;
        var l = e.alternate;
        return l === null ? (e.childLanes = 0, e.lanes = t, e.child = null, e.subtreeFlags = 0, e.memoizedProps = null, e.memoizedState = null, e.updateQueue = null, e.dependencies = null, e.stateNode = null) : (e.childLanes = l.childLanes, e.lanes = l.lanes, e.child = l.child, e.subtreeFlags = 0, e.deletions = null, e.memoizedProps = l.memoizedProps, e.memoizedState = l.memoizedState, e.updateQueue = l.updateQueue, e.type = l.type, t = l.dependencies, e.dependencies = t === null ? null : {
            lanes: t.lanes,
            firstContext: t.firstContext
        }), e
    }

    function Fn(e, t, l, a, n, u) {
        var i = 0;
        if (a = e, typeof e == "function") qi(e) && (i = 1);
        else if (typeof e == "string") i = g1(e, l, Y.current) ? 26 : e === "html" || e === "head" || e === "body" ? 27 : 5;
        else e: switch (e) {
        case ne:
            return e = vt(31, l, t, n), e.elementType = ne, e.lanes = u, e;
        case K:
            return Hl(l.children, n, u, t);
        case ae:
            i = 8, n |= 24;
            break;
        case J:
            return e = vt(12, l, t, n | 2), e.elementType = J, e.lanes = u, e;
        case W:
            return e = vt(13, l, t, n), e.elementType = W, e.lanes = u, e;
        case Q:
            return e = vt(19, l, t, n), e.elementType = Q, e.lanes = u, e;
        default:
            if (typeof e == "object" && e !== null) switch (e.$$typeof) {
            case F:
                i = 10;
                break e;
            case ze:
                i = 9;
                break e;
            case Re:
                i = 11;
                break e;
            case O:
                i = 14;
                break e;
            case U:
                i = 16, a = null;
                break e
            }
            i = 29, l = Error(o(130, e === null ? "null" : typeof e, "")), a = null
        }
        return t = vt(i, l, t, n), t.elementType = e, t.type = a, t.lanes = u, t
    }

    function Hl(e, t, l, a) {
        return e = vt(7, e, a, t), e.lanes = l, e
    }

    function Bi(e, t, l) {
        return e = vt(6, e, null, t), e.lanes = l, e
    }

    function Hf(e) {
        var t = vt(18, null, null, 0);
        return t.stateNode = e, t
    }

    function Li(e, t, l) {
        return t = vt(4, e.children !== null ? e.children : [], e.key, t), t.lanes = l, t.stateNode = {
            containerInfo: e.containerInfo,
            pendingChildren: null,
            implementation: e.implementation
        }, t
    }
    var qf = new WeakMap;

    function xt(e, t) {
        if (typeof e == "object" && e !== null) {
            var l = qf.get(e);
            return l !== void 0 ? l : (t = {
                value: e,
                source: t,
                stack: Cs(t)
            }, qf.set(e, t), t)
        }
        return {
            value: e,
            source: t,
            stack: Cs(t)
        }
    }
    var ca = [],
        sa = 0,
        In = null,
        Ja = 0,
        zt = [],
        jt = 0,
        il = null,
        Ht = 1,
        qt = "";

    function Qt(e, t) {
        ca[sa++] = Ja, ca[sa++] = In, In = e, Ja = t
    }

    function Bf(e, t, l) {
        zt[jt++] = Ht, zt[jt++] = qt, zt[jt++] = il, il = e;
        var a = Ht;
        e = qt;
        var n = 32 - mt(a) - 1;
        a &= ~(1 << n), l += 1;
        var u = 32 - mt(t) + n;
        if (30 < u) {
            var i = n - n % 5;
            u = (a & (1 << i) - 1).toString(32), a >>= i, n -= i, Ht = 1 << 32 - mt(t) + n | l << n | a, qt = u + e
        } else Ht = 1 << u | l << n | a, qt = e
    }

    function ki(e) {
        e.return !== null && (Qt(e, 1), Bf(e, 1, 0))
    }

    function Yi(e) {
        for (; e === In;) In = ca[--sa], ca[sa] = null, Ja = ca[--sa], ca[sa] = null;
        for (; e === il;) il = zt[--jt], zt[jt] = null, qt = zt[--jt], zt[jt] = null, Ht = zt[--jt], zt[jt] = null
    }

    function Lf(e, t) {
        zt[jt++] = Ht, zt[jt++] = qt, zt[jt++] = il, Ht = t.id, qt = t.overflow, il = e
    }
    var Je = null,
        Ae = null,
        re = !1,
        cl = null,
        Mt = !1,
        Gi = Error(o(519));

    function sl(e) {
        var t = Error(o(418, 1 < arguments.length && arguments[1] !== void 0 && arguments[1] ? "text" : "HTML", ""));
        throw Wa(xt(t, e)), Gi
    }

    function kf(e) {
        var t = e.stateNode,
            l = e.type,
            a = e.memoizedProps;
        switch (t[Ke] = e, t[at] = a, l) {
        case "dialog":
            ce("cancel", t), ce("close", t);
            break;
        case "iframe":
        case "object":
        case "embed":
            ce("load", t);
            break;
        case "video":
        case "audio":
            for (l = 0; l < pn.length; l++) ce(pn[l], t);
            break;
        case "source":
            ce("error", t);
            break;
        case "img":
        case "image":
        case "link":
            ce("error", t), ce("load", t);
            break;
        case "details":
            ce("toggle", t);
            break;
        case "input":
            ce("invalid", t), Fs(t, a.value, a.defaultValue, a.checked, a.defaultChecked, a.type, a.name, !0);
            break;
        case "select":
            ce("invalid", t);
            break;
        case "textarea":
            ce("invalid", t), Ps(t, a.value, a.defaultValue, a.children)
        }
        l = a.children, typeof l != "string" && typeof l != "number" && typeof l != "bigint" || t.textContent === "" + l || a.suppressHydrationWarning === !0 || ad(t.textContent, l) ? (a.popover != null && (ce("beforetoggle", t), ce("toggle", t)), a.onScroll != null && ce("scroll", t), a.onScrollEnd != null && ce("scrollend", t), a.onClick != null && (t.onclick = Yt), t = !0) : t = !1, t || sl(e, !0)
    }

    function Yf(e) {
        for (Je = e.return; Je;) switch (Je.tag) {
        case 5:
        case 31:
        case 13:
            Mt = !1;
            return;
        case 27:
        case 3:
            Mt = !0;
            return;
        default:
            Je = Je.return
        }
    }

    function fa(e) {
        if (e !== Je) return !1;
        if (!re) return Yf(e), re = !0, !1;
        var t = e.tag,
            l;
        if ((l = t !== 3 && t !== 27) && ((l = t === 5) && (l = e.type, l = !(l !== "form" && l !== "button") || us(e.type, e.memoizedProps)), l = !l), l && Ae && sl(e), Yf(e), t === 13) {
            if (e = e.memoizedState, e = e !== null ? e.dehydrated : null, !e) throw Error(o(317));
            Ae = dd(e)
        } else if (t === 31) {
            if (e = e.memoizedState, e = e !== null ? e.dehydrated : null, !e) throw Error(o(317));
            Ae = dd(e)
        } else t === 27 ? (t = Ae, El(e.type) ? (e = os, os = null, Ae = e) : Ae = t) : Ae = Je ? At(e.stateNode.nextSibling) : null;
        return !0
    }

    function ql() {
        Ae = Je = null, re = !1
    }

    function Xi() {
        var e = cl;
        return e !== null && (st === null ? st = e : st.push.apply(st, e), cl = null), e
    }

    function Wa(e) {
        cl === null ? cl = [e] : cl.push(e)
    }
    var Qi = m(null),
        Bl = null,
        Vt = null;

    function fl(e, t, l) {
        B(Qi, t._currentValue), t._currentValue = l
    }

    function wt(e) {
        e._currentValue = Qi.current, A(Qi)
    }

    function Vi(e, t, l) {
        for (; e !== null;) {
            var a = e.alternate;
            if ((e.childLanes & t) !== t ? (e.childLanes |= t, a !== null && (a.childLanes |= t)) : a !== null && (a.childLanes & t) !== t && (a.childLanes |= t), e === l) break;
            e = e.return
        }
    }

    function wi(e, t, l, a) {
        var n = e.child;
        for (n !== null && (n.return = e); n !== null;) {
            var u = n.dependencies;
            if (u !== null) {
                var i = n.child;
                u = u.firstContext;
                e: for (; u !== null;) {
                    var s = u;
                    u = n;
                    for (var r = 0; r < t.length; r++)
                        if (s.context === t[r]) {
                            u.lanes |= l, s = u.alternate, s !== null && (s.lanes |= l), Vi(u.return, l, e), a || (i = null);
                            break e
                        } u = s.next
                }
            } else if (n.tag === 18) {
                if (i = n.return, i === null) throw Error(o(341));
                i.lanes |= l, u = i.alternate, u !== null && (u.lanes |= l), Vi(i, l, e), i = null
            } else i = n.child;
            if (i !== null) i.return = n;
            else
                for (i = n; i !== null;) {
                    if (i === e) {
                        i = null;
                        break
                    }
                    if (n = i.sibling, n !== null) {
                        n.return = i.return, i = n;
                        break
                    }
                    i = i.return
                }
            n = i
        }
    }

    function oa(e, t, l, a) {
        e = null;
        for (var n = t, u = !1; n !== null;) {
            if (!u) {
                if ((n.flags & 524288) !== 0) u = !0;
                else if ((n.flags & 262144) !== 0) break
            }
            if (n.tag === 10) {
                var i = n.alternate;
                if (i === null) throw Error(o(387));
                if (i = i.memoizedProps, i !== null) {
                    var s = n.type;
                    ht(n.pendingProps.value, i.value) || (e !== null ? e.push(s) : e = [s])
                }
            } else if (n === ve.current) {
                if (i = n.alternate, i === null) throw Error(o(387));
                i.memoizedState.memoizedState !== n.memoizedState.memoizedState && (e !== null ? e.push(Tn) : e = [Tn])
            }
            n = n.return
        }
        e !== null && wi(t, e, l, a), t.flags |= 262144
    }

    function Pn(e) {
        for (e = e.firstContext; e !== null;) {
            if (!ht(e.context._currentValue, e.memoizedValue)) return !0;
            e = e.next
        }
        return !1
    }

    function Ll(e) {
        Bl = e, Vt = null, e = e.dependencies, e !== null && (e.firstContext = null)
    }

    function We(e) {
        return Gf(Bl, e)
    }

    function eu(e, t) {
        return Bl === null && Ll(e), Gf(e, t)
    }

    function Gf(e, t) {
        var l = t._currentValue;
        if (t = {
                context: t,
                memoizedValue: l,
                next: null
            }, Vt === null) {
            if (e === null) throw Error(o(308));
            Vt = t, e.dependencies = {
                lanes: 0,
                firstContext: t
            }, e.flags |= 524288
        } else Vt = Vt.next = t;
        return l
    }
    var dh = typeof AbortController < "u" ? AbortController : function () {
            var e = [],
                t = this.signal = {
                    aborted: !1,
                    addEventListener: function (l, a) {
                        e.push(a)
                    }
                };
            this.abort = function () {
                t.aborted = !0, e.forEach(function (l) {
                    return l()
                })
            }
        },
        mh = f.unstable_scheduleCallback,
        hh = f.unstable_NormalPriority,
        ke = {
            $$typeof: F,
            Consumer: null,
            Provider: null,
            _currentValue: null,
            _currentValue2: null,
            _threadCount: 0
        };

    function Zi() {
        return {
            controller: new dh,
            data: new Map,
            refCount: 0
        }
    }

    function $a(e) {
        e.refCount--, e.refCount === 0 && mh(hh, function () {
            e.controller.abort()
        })
    }
    var Fa = null,
        Ki = 0,
        ra = 0,
        da = null;

    function vh(e, t) {
        if (Fa === null) {
            var l = Fa = [];
            Ki = 0, ra = $c(), da = {
                status: "pending",
                value: void 0,
                then: function (a) {
                    l.push(a)
                }
            }
        }
        return Ki++, t.then(Xf, Xf), t
    }

    function Xf() {
        if (--Ki === 0 && Fa !== null) {
            da !== null && (da.status = "fulfilled");
            var e = Fa;
            Fa = null, ra = 0, da = null;
            for (var t = 0; t < e.length; t++)(0, e[t])()
        }
    }

    function gh(e, t) {
        var l = [],
            a = {
                status: "pending",
                value: null,
                reason: null,
                then: function (n) {
                    l.push(n)
                }
            };
        return e.then(function () {
            a.status = "fulfilled", a.value = t;
            for (var n = 0; n < l.length; n++)(0, l[n])(t)
        }, function (n) {
            for (a.status = "rejected", a.reason = n, n = 0; n < l.length; n++)(0, l[n])(void 0)
        }), a
    }
    var Qf = x.S;
    x.S = function (e, t) {
        Mr = rt(), typeof t == "object" && t !== null && typeof t.then == "function" && vh(e, t), Qf !== null && Qf(e, t)
    };
    var kl = m(null);

    function Ji() {
        var e = kl.current;
        return e !== null ? e : xe.pooledCache
    }

    function tu(e, t) {
        t === null ? B(kl, kl.current) : B(kl, t.pool)
    }

    function Vf() {
        var e = Ji();
        return e === null ? null : {
            parent: ke._currentValue,
            pool: e
        }
    }
    var ma = Error(o(460)),
        Wi = Error(o(474)),
        lu = Error(o(542)),
        au = {
            then: function () {}
        };

    function wf(e) {
        return e = e.status, e === "fulfilled" || e === "rejected"
    }

    function Zf(e, t, l) {
        switch (l = e[l], l === void 0 ? e.push(t) : l !== t && (t.then(Yt, Yt), t = l), t.status) {
        case "fulfilled":
            return t.value;
        case "rejected":
            throw e = t.reason, Jf(e), e;
        default:
            if (typeof t.status == "string") t.then(Yt, Yt);
            else {
                if (e = xe, e !== null && 100 < e.shellSuspendCounter) throw Error(o(482));
                e = t, e.status = "pending", e.then(function (a) {
                    if (t.status === "pending") {
                        var n = t;
                        n.status = "fulfilled", n.value = a
                    }
                }, function (a) {
                    if (t.status === "pending") {
                        var n = t;
                        n.status = "rejected", n.reason = a
                    }
                })
            }
            switch (t.status) {
            case "fulfilled":
                return t.value;
            case "rejected":
                throw e = t.reason, Jf(e), e
            }
            throw Gl = t, ma
        }
    }

    function Yl(e) {
        try {
            var t = e._init;
            return t(e._payload)
        } catch (l) {
            throw l !== null && typeof l == "object" && typeof l.then == "function" ? (Gl = l, ma) : l
        }
    }
    var Gl = null;

    function Kf() {
        if (Gl === null) throw Error(o(459));
        var e = Gl;
        return Gl = null, e
    }

    function Jf(e) {
        if (e === ma || e === lu) throw Error(o(483))
    }
    var ha = null,
        Ia = 0;

    function nu(e) {
        var t = Ia;
        return Ia += 1, ha === null && (ha = []), Zf(ha, e, t)
    }

    function Pa(e, t) {
        t = t.props.ref, e.ref = t !== void 0 ? t : null
    }

    function uu(e, t) {
        throw t.$$typeof === X ? Error(o(525)) : (e = Object.prototype.toString.call(t), Error(o(31, e === "[object Object]" ? "object with keys {" + Object.keys(t).join(", ") + "}" : e)))
    }

    function Wf(e) {
        function t(v, d) {
            if (e) {
                var g = v.deletions;
                g === null ? (v.deletions = [d], v.flags |= 16) : g.push(d)
            }
        }

        function l(v, d) {
            if (!e) return null;
            for (; d !== null;) t(v, d), d = d.sibling;
            return null
        }

        function a(v) {
            for (var d = new Map; v !== null;) v.key !== null ? d.set(v.key, v) : d.set(v.index, v), v = v.sibling;
            return d
        }

        function n(v, d) {
            return v = Xt(v, d), v.index = 0, v.sibling = null, v
        }

        function u(v, d, g) {
            return v.index = g, e ? (g = v.alternate, g !== null ? (g = g.index, g < d ? (v.flags |= 67108866, d) : g) : (v.flags |= 67108866, d)) : (v.flags |= 1048576, d)
        }

        function i(v) {
            return e && v.alternate === null && (v.flags |= 67108866), v
        }

        function s(v, d, g, j) {
            return d === null || d.tag !== 6 ? (d = Bi(g, v.mode, j), d.return = v, d) : (d = n(d, g), d.return = v, d)
        }

        function r(v, d, g, j) {
            var Z = g.type;
            return Z === K ? T(v, d, g.props.children, j, g.key) : d !== null && (d.elementType === Z || typeof Z == "object" && Z !== null && Z.$$typeof === U && Yl(Z) === d.type) ? (d = n(d, g.props), Pa(d, g), d.return = v, d) : (d = Fn(g.type, g.key, g.props, null, v.mode, j), Pa(d, g), d.return = v, d)
        }

        function y(v, d, g, j) {
            return d === null || d.tag !== 4 || d.stateNode.containerInfo !== g.containerInfo || d.stateNode.implementation !== g.implementation ? (d = Li(g, v.mode, j), d.return = v, d) : (d = n(d, g.children || []), d.return = v, d)
        }

        function T(v, d, g, j, Z) {
            return d === null || d.tag !== 7 ? (d = Hl(g, v.mode, j, Z), d.return = v, d) : (d = n(d, g), d.return = v, d)
        }

        function D(v, d, g) {
            if (typeof d == "string" && d !== "" || typeof d == "number" || typeof d == "bigint") return d = Bi("" + d, v.mode, g), d.return = v, d;
            if (typeof d == "object" && d !== null) {
                switch (d.$$typeof) {
                case w:
                    return g = Fn(d.type, d.key, d.props, null, v.mode, g), Pa(g, d), g.return = v, g;
                case V:
                    return d = Li(d, v.mode, g), d.return = v, d;
                case U:
                    return d = Yl(d), D(v, d, g)
                }
                if (De(d) || Me(d)) return d = Hl(d, v.mode, g, null), d.return = v, d;
                if (typeof d.then == "function") return D(v, nu(d), g);
                if (d.$$typeof === F) return D(v, eu(v, d), g);
                uu(v, d)
            }
            return null
        }

        function p(v, d, g, j) {
            var Z = d !== null ? d.key : null;
            if (typeof g == "string" && g !== "" || typeof g == "number" || typeof g == "bigint") return Z !== null ? null : s(v, d, "" + g, j);
            if (typeof g == "object" && g !== null) {
                switch (g.$$typeof) {
                case w:
                    return g.key === Z ? r(v, d, g, j) : null;
                case V:
                    return g.key === Z ? y(v, d, g, j) : null;
                case U:
                    return g = Yl(g), p(v, d, g, j)
                }
                if (De(g) || Me(g)) return Z !== null ? null : T(v, d, g, j, null);
                if (typeof g.then == "function") return p(v, d, nu(g), j);
                if (g.$$typeof === F) return p(v, d, eu(v, g), j);
                uu(v, g)
            }
            return null
        }

        function E(v, d, g, j, Z) {
            if (typeof j == "string" && j !== "" || typeof j == "number" || typeof j == "bigint") return v = v.get(g) || null, s(d, v, "" + j, Z);
            if (typeof j == "object" && j !== null) {
                switch (j.$$typeof) {
                case w:
                    return v = v.get(j.key === null ? g : j.key) || null, r(d, v, j, Z);
                case V:
                    return v = v.get(j.key === null ? g : j.key) || null, y(d, v, j, Z);
                case U:
                    return j = Yl(j), E(v, d, g, j, Z)
                }
                if (De(j) || Me(j)) return v = v.get(g) || null, T(d, v, j, Z, null);
                if (typeof j.then == "function") return E(v, d, g, nu(j), Z);
                if (j.$$typeof === F) return E(v, d, g, eu(d, j), Z);
                uu(d, j)
            }
            return null
        }

        function k(v, d, g, j) {
            for (var Z = null, de = null, G = d, le = d = 0, oe = null; G !== null && le < g.length; le++) {
                G.index > le ? (oe = G, G = null) : oe = G.sibling;
                var me = p(v, G, g[le], j);
                if (me === null) {
                    G === null && (G = oe);
                    break
                }
                e && G && me.alternate === null && t(v, G), d = u(me, d, le), de === null ? Z = me : de.sibling = me, de = me, G = oe
            }
            if (le === g.length) return l(v, G), re && Qt(v, le), Z;
            if (G === null) {
                for (; le < g.length; le++) G = D(v, g[le], j), G !== null && (d = u(G, d, le), de === null ? Z = G : de.sibling = G, de = G);
                return re && Qt(v, le), Z
            }
            for (G = a(G); le < g.length; le++) oe = E(G, v, le, g[le], j), oe !== null && (e && oe.alternate !== null && G.delete(oe.key === null ? le : oe.key), d = u(oe, d, le), de === null ? Z = oe : de.sibling = oe, de = oe);
            return e && G.forEach(function (Ml) {
                return t(v, Ml)
            }), re && Qt(v, le), Z
        }

        function $(v, d, g, j) {
            if (g == null) throw Error(o(151));
            for (var Z = null, de = null, G = d, le = d = 0, oe = null, me = g.next(); G !== null && !me.done; le++, me = g.next()) {
                G.index > le ? (oe = G, G = null) : oe = G.sibling;
                var Ml = p(v, G, me.value, j);
                if (Ml === null) {
                    G === null && (G = oe);
                    break
                }
                e && G && Ml.alternate === null && t(v, G), d = u(Ml, d, le), de === null ? Z = Ml : de.sibling = Ml, de = Ml, G = oe
            }
            if (me.done) return l(v, G), re && Qt(v, le), Z;
            if (G === null) {
                for (; !me.done; le++, me = g.next()) me = D(v, me.value, j), me !== null && (d = u(me, d, le), de === null ? Z = me : de.sibling = me, de = me);
                return re && Qt(v, le), Z
            }
            for (G = a(G); !me.done; le++, me = g.next()) me = E(G, v, le, me.value, j), me !== null && (e && me.alternate !== null && G.delete(me.key === null ? le : me.key), d = u(me, d, le), de === null ? Z = me : de.sibling = me, de = me);
            return e && G.forEach(function (M1) {
                return t(v, M1)
            }), re && Qt(v, le), Z
        }

        function Ee(v, d, g, j) {
            if (typeof g == "object" && g !== null && g.type === K && g.key === null && (g = g.props.children), typeof g == "object" && g !== null) {
                switch (g.$$typeof) {
                case w:
                    e: {
                        for (var Z = g.key; d !== null;) {
                            if (d.key === Z) {
                                if (Z = g.type, Z === K) {
                                    if (d.tag === 7) {
                                        l(v, d.sibling), j = n(d, g.props.children), j.return = v, v = j;
                                        break e
                                    }
                                } else if (d.elementType === Z || typeof Z == "object" && Z !== null && Z.$$typeof === U && Yl(Z) === d.type) {
                                    l(v, d.sibling), j = n(d, g.props), Pa(j, g), j.return = v, v = j;
                                    break e
                                }
                                l(v, d);
                                break
                            } else t(v, d);
                            d = d.sibling
                        }
                        g.type === K ? (j = Hl(g.props.children, v.mode, j, g.key), j.return = v, v = j) : (j = Fn(g.type, g.key, g.props, null, v.mode, j), Pa(j, g), j.return = v, v = j)
                    }
                    return i(v);
                case V:
                    e: {
                        for (Z = g.key; d !== null;) {
                            if (d.key === Z)
                                if (d.tag === 4 && d.stateNode.containerInfo === g.containerInfo && d.stateNode.implementation === g.implementation) {
                                    l(v, d.sibling), j = n(d, g.children || []), j.return = v, v = j;
                                    break e
                                } else {
                                    l(v, d);
                                    break
                                }
                            else t(v, d);
                            d = d.sibling
                        }
                        j = Li(g, v.mode, j),
                        j.return = v,
                        v = j
                    }
                    return i(v);
                case U:
                    return g = Yl(g), Ee(v, d, g, j)
                }
                if (De(g)) return k(v, d, g, j);
                if (Me(g)) {
                    if (Z = Me(g), typeof Z != "function") throw Error(o(150));
                    return g = Z.call(g), $(v, d, g, j)
                }
                if (typeof g.then == "function") return Ee(v, d, nu(g), j);
                if (g.$$typeof === F) return Ee(v, d, eu(v, g), j);
                uu(v, g)
            }
            return typeof g == "string" && g !== "" || typeof g == "number" || typeof g == "bigint" ? (g = "" + g, d !== null && d.tag === 6 ? (l(v, d.sibling), j = n(d, g), j.return = v, v = j) : (l(v, d), j = Bi(g, v.mode, j), j.return = v, v = j), i(v)) : l(v, d)
        }
        return function (v, d, g, j) {
            try {
                Ia = 0;
                var Z = Ee(v, d, g, j);
                return ha = null, Z
            } catch (G) {
                if (G === ma || G === lu) throw G;
                var de = vt(29, G, null, v.mode);
                return de.lanes = j, de.return = v, de
            }
        }
    }
    var Xl = Wf(!0),
        $f = Wf(!1),
        ol = !1;

    function $i(e) {
        e.updateQueue = {
            baseState: e.memoizedState,
            firstBaseUpdate: null,
            lastBaseUpdate: null,
            shared: {
                pending: null,
                lanes: 0,
                hiddenCallbacks: null
            },
            callbacks: null
        }
    }

    function Fi(e, t) {
        e = e.updateQueue, t.updateQueue === e && (t.updateQueue = {
            baseState: e.baseState,
            firstBaseUpdate: e.firstBaseUpdate,
            lastBaseUpdate: e.lastBaseUpdate,
            shared: e.shared,
            callbacks: null
        })
    }

    function rl(e) {
        return {
            lane: e,
            tag: 0,
            payload: null,
            callback: null,
            next: null
        }
    }

    function dl(e, t, l) {
        var a = e.updateQueue;
        if (a === null) return null;
        if (a = a.shared, (he & 2) !== 0) {
            var n = a.pending;
            return n === null ? t.next = t : (t.next = n.next, n.next = t), a.pending = t, t = $n(e), Uf(e, null, l), t
        }
        return Wn(e, a, t, l), $n(e)
    }

    function en(e, t, l) {
        if (t = t.updateQueue, t !== null && (t = t.shared, (l & 4194048) !== 0)) {
            var a = t.lanes;
            a &= e.pendingLanes, l |= a, t.lanes = l, Ys(e, l)
        }
    }

    function Ii(e, t) {
        var l = e.updateQueue,
            a = e.alternate;
        if (a !== null && (a = a.updateQueue, l === a)) {
            var n = null,
                u = null;
            if (l = l.firstBaseUpdate, l !== null) {
                do {
                    var i = {
                        lane: l.lane,
                        tag: l.tag,
                        payload: l.payload,
                        callback: null,
                        next: null
                    };
                    u === null ? n = u = i : u = u.next = i, l = l.next
                } while (l !== null);
                u === null ? n = u = t : u = u.next = t
            } else n = u = t;
            l = {
                baseState: a.baseState,
                firstBaseUpdate: n,
                lastBaseUpdate: u,
                shared: a.shared,
                callbacks: a.callbacks
            }, e.updateQueue = l;
            return
        }
        e = l.lastBaseUpdate, e === null ? l.firstBaseUpdate = t : e.next = t, l.lastBaseUpdate = t
    }
    var Pi = !1;

    function tn() {
        if (Pi) {
            var e = da;
            if (e !== null) throw e
        }
    }

    function ln(e, t, l, a) {
        Pi = !1;
        var n = e.updateQueue;
        ol = !1;
        var u = n.firstBaseUpdate,
            i = n.lastBaseUpdate,
            s = n.shared.pending;
        if (s !== null) {
            n.shared.pending = null;
            var r = s,
                y = r.next;
            r.next = null, i === null ? u = y : i.next = y, i = r;
            var T = e.alternate;
            T !== null && (T = T.updateQueue, s = T.lastBaseUpdate, s !== i && (s === null ? T.firstBaseUpdate = y : s.next = y, T.lastBaseUpdate = r))
        }
        if (u !== null) {
            var D = n.baseState;
            i = 0, T = y = r = null, s = u;
            do {
                var p = s.lane & -536870913,
                    E = p !== s.lane;
                if (E ? (fe & p) === p : (a & p) === p) {
                    p !== 0 && p === ra && (Pi = !0), T !== null && (T = T.next = {
                        lane: 0,
                        tag: s.tag,
                        payload: s.payload,
                        callback: null,
                        next: null
                    });
                    e: {
                        var k = e,
                            $ = s;p = t;
                        var Ee = l;
                        switch ($.tag) {
                        case 1:
                            if (k = $.payload, typeof k == "function") {
                                D = k.call(Ee, D, p);
                                break e
                            }
                            D = k;
                            break e;
                        case 3:
                            k.flags = k.flags & -65537 | 128;
                        case 0:
                            if (k = $.payload, p = typeof k == "function" ? k.call(Ee, D, p) : k, p == null) break e;
                            D = M({}, D, p);
                            break e;
                        case 2:
                            ol = !0
                        }
                    }
                    p = s.callback, p !== null && (e.flags |= 64, E && (e.flags |= 8192), E = n.callbacks, E === null ? n.callbacks = [p] : E.push(p))
                } else E = {
                    lane: p,
                    tag: s.tag,
                    payload: s.payload,
                    callback: s.callback,
                    next: null
                }, T === null ? (y = T = E, r = D) : T = T.next = E, i |= p;
                if (s = s.next, s === null) {
                    if (s = n.shared.pending, s === null) break;
                    E = s, s = E.next, E.next = null, n.lastBaseUpdate = E, n.shared.pending = null
                }
            } while (!0);
            T === null && (r = D), n.baseState = r, n.firstBaseUpdate = y, n.lastBaseUpdate = T, u === null && (n.shared.lanes = 0), yl |= i, e.lanes = i, e.memoizedState = D
        }
    }

    function Ff(e, t) {
        if (typeof e != "function") throw Error(o(191, e));
        e.call(t)
    }

    function If(e, t) {
        var l = e.callbacks;
        if (l !== null)
            for (e.callbacks = null, e = 0; e < l.length; e++) Ff(l[e], t)
    }
    var va = m(null),
        iu = m(0);

    function Pf(e, t) {
        e = el, B(iu, e), B(va, t), el = e | t.baseLanes
    }

    function ec() {
        B(iu, el), B(va, va.current)
    }

    function tc() {
        el = iu.current, A(va), A(iu)
    }
    var gt = m(null),
        Dt = null;

    function ml(e) {
        var t = e.alternate;
        B(Be, Be.current & 1), B(gt, e), Dt === null && (t === null || va.current !== null || t.memoizedState !== null) && (Dt = e)
    }

    function lc(e) {
        B(Be, Be.current), B(gt, e), Dt === null && (Dt = e)
    }

    function eo(e) {
        e.tag === 22 ? (B(Be, Be.current), B(gt, e), Dt === null && (Dt = e)) : hl()
    }

    function hl() {
        B(Be, Be.current), B(gt, gt.current)
    }

    function yt(e) {
        A(gt), Dt === e && (Dt = null), A(Be)
    }
    var Be = m(0);

    function cu(e) {
        for (var t = e; t !== null;) {
            if (t.tag === 13) {
                var l = t.memoizedState;
                if (l !== null && (l = l.dehydrated, l === null || ss(l) || fs(l))) return t
            } else if (t.tag === 19 && (t.memoizedProps.revealOrder === "forwards" || t.memoizedProps.revealOrder === "backwards" || t.memoizedProps.revealOrder === "unstable_legacy-backwards" || t.memoizedProps.revealOrder === "together")) {
                if ((t.flags & 128) !== 0) return t
            } else if (t.child !== null) {
                t.child.return = t, t = t.child;
                continue
            }
            if (t === e) break;
            for (; t.sibling === null;) {
                if (t.return === null || t.return === e) return null;
                t = t.return
            }
            t.sibling.return = t.return, t = t.sibling
        }
        return null
    }
    var Zt = 0,
        te = null,
        be = null,
        Ye = null,
        su = !1,
        ga = !1,
        Ql = !1,
        fu = 0,
        an = 0,
        ya = null,
        yh = 0;

    function Ce() {
        throw Error(o(321))
    }

    function ac(e, t) {
        if (t === null) return !1;
        for (var l = 0; l < t.length && l < e.length; l++)
            if (!ht(e[l], t[l])) return !1;
        return !0
    }

    function nc(e, t, l, a, n, u) {
        return Zt = u, te = t, t.memoizedState = null, t.updateQueue = null, t.lanes = 0, x.H = e === null || e.memoizedState === null ? Lo : Sc, Ql = !1, u = l(a, n), Ql = !1, ga && (u = lo(t, l, a, n)), to(e), u
    }

    function to(e) {
        x.H = cn;
        var t = be !== null && be.next !== null;
        if (Zt = 0, Ye = be = te = null, su = !1, an = 0, ya = null, t) throw Error(o(300));
        e === null || Ge || (e = e.dependencies, e !== null && Pn(e) && (Ge = !0))
    }

    function lo(e, t, l, a) {
        te = e;
        var n = 0;
        do {
            if (ga && (ya = null), an = 0, ga = !1, 25 <= n) throw Error(o(301));
            if (n += 1, Ye = be = null, e.updateQueue != null) {
                var u = e.updateQueue;
                u.lastEffect = null, u.events = null, u.stores = null, u.memoCache != null && (u.memoCache.index = 0)
            }
            x.H = ko, u = t(l, a)
        } while (ga);
        return u
    }

    function ph() {
        var e = x.H,
            t = e.useState()[0];
        return t = typeof t.then == "function" ? nn(t) : t, e = e.useState()[0], (be !== null ? be.memoizedState : null) !== e && (te.flags |= 1024), t
    }

    function uc() {
        var e = fu !== 0;
        return fu = 0, e
    }

    function ic(e, t, l) {
        t.updateQueue = e.updateQueue, t.flags &= -2053, e.lanes &= ~l
    }

    function cc(e) {
        if (su) {
            for (e = e.memoizedState; e !== null;) {
                var t = e.queue;
                t !== null && (t.pending = null), e = e.next
            }
            su = !1
        }
        Zt = 0, Ye = be = te = null, ga = !1, an = fu = 0, ya = null
    }

    function lt() {
        var e = {
            memoizedState: null,
            baseState: null,
            baseQueue: null,
            queue: null,
            next: null
        };
        return Ye === null ? te.memoizedState = Ye = e : Ye = Ye.next = e, Ye
    }

    function Le() {
        if (be === null) {
            var e = te.alternate;
            e = e !== null ? e.memoizedState : null
        } else e = be.next;
        var t = Ye === null ? te.memoizedState : Ye.next;
        if (t !== null) Ye = t, be = e;
        else {
            if (e === null) throw te.alternate === null ? Error(o(467)) : Error(o(310));
            be = e, e = {
                memoizedState: be.memoizedState,
                baseState: be.baseState,
                baseQueue: be.baseQueue,
                queue: be.queue,
                next: null
            }, Ye === null ? te.memoizedState = Ye = e : Ye = Ye.next = e
        }
        return Ye
    }

    function ou() {
        return {
            lastEffect: null,
            events: null,
            stores: null,
            memoCache: null
        }
    }

    function nn(e) {
        var t = an;
        return an += 1, ya === null && (ya = []), e = Zf(ya, e, t), t = te, (Ye === null ? t.memoizedState : Ye.next) === null && (t = t.alternate, x.H = t === null || t.memoizedState === null ? Lo : Sc), e
    }

    function ru(e) {
        if (e !== null && typeof e == "object") {
            if (typeof e.then == "function") return nn(e);
            if (e.$$typeof === F) return We(e)
        }
        throw Error(o(438, String(e)))
    }

    function sc(e) {
        var t = null,
            l = te.updateQueue;
        if (l !== null && (t = l.memoCache), t == null) {
            var a = te.alternate;
            a !== null && (a = a.updateQueue, a !== null && (a = a.memoCache, a != null && (t = {
                data: a.data.map(function (n) {
                    return n.slice()
                }),
                index: 0
            })))
        }
        if (t == null && (t = {
                data: [],
                index: 0
            }), l === null && (l = ou(), te.updateQueue = l), l.memoCache = t, l = t.data[t.index], l === void 0)
            for (l = t.data[t.index] = Array(e), a = 0; a < e; a++) l[a] = Ue;
        return t.index++, l
    }

    function Kt(e, t) {
        return typeof t == "function" ? t(e) : t
    }

    function du(e) {
        var t = Le();
        return fc(t, be, e)
    }

    function fc(e, t, l) {
        var a = e.queue;
        if (a === null) throw Error(o(311));
        a.lastRenderedReducer = l;
        var n = e.baseQueue,
            u = a.pending;
        if (u !== null) {
            if (n !== null) {
                var i = n.next;
                n.next = u.next, u.next = i
            }
            t.baseQueue = n = u, a.pending = null
        }
        if (u = e.baseState, n === null) e.memoizedState = u;
        else {
            t = n.next;
            var s = i = null,
                r = null,
                y = t,
                T = !1;
            do {
                var D = y.lane & -536870913;
                if (D !== y.lane ? (fe & D) === D : (Zt & D) === D) {
                    var p = y.revertLane;
                    if (p === 0) r !== null && (r = r.next = {
                        lane: 0,
                        revertLane: 0,
                        gesture: null,
                        action: y.action,
                        hasEagerState: y.hasEagerState,
                        eagerState: y.eagerState,
                        next: null
                    }), D === ra && (T = !0);
                    else if ((Zt & p) === p) {
                        y = y.next, p === ra && (T = !0);
                        continue
                    } else D = {
                        lane: 0,
                        revertLane: y.revertLane,
                        gesture: null,
                        action: y.action,
                        hasEagerState: y.hasEagerState,
                        eagerState: y.eagerState,
                        next: null
                    }, r === null ? (s = r = D, i = u) : r = r.next = D, te.lanes |= p, yl |= p;
                    D = y.action, Ql && l(u, D), u = y.hasEagerState ? y.eagerState : l(u, D)
                } else p = {
                    lane: D,
                    revertLane: y.revertLane,
                    gesture: y.gesture,
                    action: y.action,
                    hasEagerState: y.hasEagerState,
                    eagerState: y.eagerState,
                    next: null
                }, r === null ? (s = r = p, i = u) : r = r.next = p, te.lanes |= D, yl |= D;
                y = y.next
            } while (y !== null && y !== t);
            if (r === null ? i = u : r.next = s, !ht(u, e.memoizedState) && (Ge = !0, T && (l = da, l !== null))) throw l;
            e.memoizedState = u, e.baseState = i, e.baseQueue = r, a.lastRenderedState = u
        }
        return n === null && (a.lanes = 0), [e.memoizedState, a.dispatch]
    }

    function oc(e) {
        var t = Le(),
            l = t.queue;
        if (l === null) throw Error(o(311));
        l.lastRenderedReducer = e;
        var a = l.dispatch,
            n = l.pending,
            u = t.memoizedState;
        if (n !== null) {
            l.pending = null;
            var i = n = n.next;
            do u = e(u, i.action), i = i.next; while (i !== n);
            ht(u, t.memoizedState) || (Ge = !0), t.memoizedState = u, t.baseQueue === null && (t.baseState = u), l.lastRenderedState = u
        }
        return [u, a]
    }

    function ao(e, t, l) {
        var a = te,
            n = Le(),
            u = re;
        if (u) {
            if (l === void 0) throw Error(o(407));
            l = l()
        } else l = t();
        var i = !ht((be || n).memoizedState, l);
        if (i && (n.memoizedState = l, Ge = !0), n = n.queue, mc(io.bind(null, a, n, e), [e]), n.getSnapshot !== t || i || Ye !== null && Ye.memoizedState.tag & 1) {
            if (a.flags |= 2048, pa(9, {
                    destroy: void 0
                }, uo.bind(null, a, n, l, t), null), xe === null) throw Error(o(349));
            u || (Zt & 127) !== 0 || no(a, t, l)
        }
        return l
    }

    function no(e, t, l) {
        e.flags |= 16384, e = {
            getSnapshot: t,
            value: l
        }, t = te.updateQueue, t === null ? (t = ou(), te.updateQueue = t, t.stores = [e]) : (l = t.stores, l === null ? t.stores = [e] : l.push(e))
    }

    function uo(e, t, l, a) {
        t.value = l, t.getSnapshot = a, co(t) && so(e)
    }

    function io(e, t, l) {
        return l(function () {
            co(t) && so(e)
        })
    }

    function co(e) {
        var t = e.getSnapshot;
        e = e.value;
        try {
            var l = t();
            return !ht(e, l)
        } catch {
            return !0
        }
    }

    function so(e) {
        var t = Cl(e, 2);
        t !== null && ft(t, e, 2)
    }

    function rc(e) {
        var t = lt();
        if (typeof e == "function") {
            var l = e;
            if (e = l(), Ql) {
                al(!0);
                try {
                    l()
                } finally {
                    al(!1)
                }
            }
        }
        return t.memoizedState = t.baseState = e, t.queue = {
            pending: null,
            lanes: 0,
            dispatch: null,
            lastRenderedReducer: Kt,
            lastRenderedState: e
        }, t
    }

    function fo(e, t, l, a) {
        return e.baseState = l, fc(e, be, typeof a == "function" ? a : Kt)
    }

    function Sh(e, t, l, a, n) {
        if (vu(e)) throw Error(o(485));
        if (e = t.action, e !== null) {
            var u = {
                payload: n,
                action: e,
                next: null,
                isTransition: !0,
                status: "pending",
                value: null,
                reason: null,
                listeners: [],
                then: function (i) {
                    u.listeners.push(i)
                }
            };
            x.T !== null ? l(!0) : u.isTransition = !1, a(u), l = t.pending, l === null ? (u.next = t.pending = u, oo(t, u)) : (u.next = l.next, t.pending = l.next = u)
        }
    }

    function oo(e, t) {
        var l = t.action,
            a = t.payload,
            n = e.state;
        if (t.isTransition) {
            var u = x.T,
                i = {};
            x.T = i;
            try {
                var s = l(n, a),
                    r = x.S;
                r !== null && r(i, s), ro(e, t, s)
            } catch (y) {
                dc(e, t, y)
            } finally {
                u !== null && i.types !== null && (u.types = i.types), x.T = u
            }
        } else try {
            u = l(n, a), ro(e, t, u)
        } catch (y) {
            dc(e, t, y)
        }
    }

    function ro(e, t, l) {
        l !== null && typeof l == "object" && typeof l.then == "function" ? l.then(function (a) {
            mo(e, t, a)
        }, function (a) {
            return dc(e, t, a)
        }) : mo(e, t, l)
    }

    function mo(e, t, l) {
        t.status = "fulfilled", t.value = l, ho(t), e.state = l, t = e.pending, t !== null && (l = t.next, l === t ? e.pending = null : (l = l.next, t.next = l, oo(e, l)))
    }

    function dc(e, t, l) {
        var a = e.pending;
        if (e.pending = null, a !== null) {
            a = a.next;
            do t.status = "rejected", t.reason = l, ho(t), t = t.next; while (t !== a)
        }
        e.action = null
    }

    function ho(e) {
        e = e.listeners;
        for (var t = 0; t < e.length; t++)(0, e[t])()
    }

    function vo(e, t) {
        return t
    }

    function go(e, t) {
        if (re) {
            var l = xe.formState;
            if (l !== null) {
                e: {
                    var a = te;
                    if (re) {
                        if (Ae) {
                            t: {
                                for (var n = Ae, u = Mt; n.nodeType !== 8;) {
                                    if (!u) {
                                        n = null;
                                        break t
                                    }
                                    if (n = At(n.nextSibling), n === null) {
                                        n = null;
                                        break t
                                    }
                                }
                                u = n.data,
                                n = u === "F!" || u === "F" ? n : null
                            }
                            if (n) {
                                Ae = At(n.nextSibling), a = n.data === "F!";
                                break e
                            }
                        }
                        sl(a)
                    }
                    a = !1
                }
                a && (t = l[0])
            }
        }
        return l = lt(), l.memoizedState = l.baseState = t, a = {
            pending: null,
            lanes: 0,
            dispatch: null,
            lastRenderedReducer: vo,
            lastRenderedState: t
        }, l.queue = a, l = Ho.bind(null, te, a), a.dispatch = l, a = rc(!1), u = pc.bind(null, te, !1, a.queue), a = lt(), n = {
            state: t,
            dispatch: null,
            action: e,
            pending: null
        }, a.queue = n, l = Sh.bind(null, te, n, u, l), n.dispatch = l, a.memoizedState = e, [t, l, !1]
    }

    function yo(e) {
        var t = Le();
        return po(t, be, e)
    }

    function po(e, t, l) {
        if (t = fc(e, t, vo)[0], e = du(Kt)[0], typeof t == "object" && t !== null && typeof t.then == "function") try {
            var a = nn(t)
        } catch (i) {
            throw i === ma ? lu : i
        } else a = t;
        t = Le();
        var n = t.queue,
            u = n.dispatch;
        return l !== t.memoizedState && (te.flags |= 2048, pa(9, {
            destroy: void 0
        }, bh.bind(null, n, l), null)), [a, u, e]
    }

    function bh(e, t) {
        e.action = t
    }

    function So(e) {
        var t = Le(),
            l = be;
        if (l !== null) return po(t, l, e);
        Le(), t = t.memoizedState, l = Le();
        var a = l.queue.dispatch;
        return l.memoizedState = e, [t, a, !1]
    }

    function pa(e, t, l, a) {
        return e = {
            tag: e,
            create: l,
            deps: a,
            inst: t,
            next: null
        }, t = te.updateQueue, t === null && (t = ou(), te.updateQueue = t), l = t.lastEffect, l === null ? t.lastEffect = e.next = e : (a = l.next, l.next = e, e.next = a, t.lastEffect = e), e
    }

    function bo() {
        return Le().memoizedState
    }

    function mu(e, t, l, a) {
        var n = lt();
        te.flags |= e, n.memoizedState = pa(1 | t, {
            destroy: void 0
        }, l, a === void 0 ? null : a)
    }

    function hu(e, t, l, a) {
        var n = Le();
        a = a === void 0 ? null : a;
        var u = n.memoizedState.inst;
        be !== null && a !== null && ac(a, be.memoizedState.deps) ? n.memoizedState = pa(t, u, l, a) : (te.flags |= e, n.memoizedState = pa(1 | t, u, l, a))
    }

    function No(e, t) {
        mu(8390656, 8, e, t)
    }

    function mc(e, t) {
        hu(2048, 8, e, t)
    }

    function Nh(e) {
        te.flags |= 4;
        var t = te.updateQueue;
        if (t === null) t = ou(), te.updateQueue = t, t.events = [e];
        else {
            var l = t.events;
            l === null ? t.events = [e] : l.push(e)
        }
    }

    function Eo(e) {
        var t = Le().memoizedState;
        return Nh({
                ref: t,
                nextImpl: e
            }),
            function () {
                if ((he & 2) !== 0) throw Error(o(440));
                return t.impl.apply(void 0, arguments)
            }
    }

    function To(e, t) {
        return hu(4, 2, e, t)
    }

    function xo(e, t) {
        return hu(4, 4, e, t)
    }

    function zo(e, t) {
        if (typeof t == "function") {
            e = e();
            var l = t(e);
            return function () {
                typeof l == "function" ? l() : t(null)
            }
        }
        if (t != null) return e = e(), t.current = e,
            function () {
                t.current = null
            }
    }

    function jo(e, t, l) {
        l = l != null ? l.concat([e]) : null, hu(4, 4, zo.bind(null, t, e), l)
    }

    function hc() {}

    function Mo(e, t) {
        var l = Le();
        t = t === void 0 ? null : t;
        var a = l.memoizedState;
        return t !== null && ac(t, a[1]) ? a[0] : (l.memoizedState = [e, t], e)
    }

    function Do(e, t) {
        var l = Le();
        t = t === void 0 ? null : t;
        var a = l.memoizedState;
        if (t !== null && ac(t, a[1])) return a[0];
        if (a = e(), Ql) {
            al(!0);
            try {
                e()
            } finally {
                al(!1)
            }
        }
        return l.memoizedState = [a, t], a
    }

    function vc(e, t, l) {
        return l === void 0 || (Zt & 1073741824) !== 0 && (fe & 261930) === 0 ? e.memoizedState = t : (e.memoizedState = l, e = Ar(), te.lanes |= e, yl |= e, l)
    }

    function Ao(e, t, l, a) {
        return ht(l, t) ? l : va.current !== null ? (e = vc(e, l, a), ht(e, t) || (Ge = !0), e) : (Zt & 42) === 0 || (Zt & 1073741824) !== 0 && (fe & 261930) === 0 ? (Ge = !0, e.memoizedState = l) : (e = Ar(), te.lanes |= e, yl |= e, t)
    }

    function _o(e, t, l, a, n) {
        var u = H.p;
        H.p = u !== 0 && 8 > u ? u : 8;
        var i = x.T,
            s = {};
        x.T = s, pc(e, !1, t, l);
        try {
            var r = n(),
                y = x.S;
            if (y !== null && y(s, r), r !== null && typeof r == "object" && typeof r.then == "function") {
                var T = gh(r, a);
                un(e, t, T, bt(e))
            } else un(e, t, a, bt(e))
        } catch (D) {
            un(e, t, {
                then: function () {},
                status: "rejected",
                reason: D
            }, bt())
        } finally {
            H.p = u, i !== null && s.types !== null && (i.types = s.types), x.T = i
        }
    }

    function Eh() {}

    function gc(e, t, l, a) {
        if (e.tag !== 5) throw Error(o(476));
        var n = Oo(e).queue;
        _o(e, n, t, I, l === null ? Eh : function () {
            return Ro(e), l(a)
        })
    }

    function Oo(e) {
        var t = e.memoizedState;
        if (t !== null) return t;
        t = {
            memoizedState: I,
            baseState: I,
            baseQueue: null,
            queue: {
                pending: null,
                lanes: 0,
                dispatch: null,
                lastRenderedReducer: Kt,
                lastRenderedState: I
            },
            next: null
        };
        var l = {};
        return t.next = {
            memoizedState: l,
            baseState: l,
            baseQueue: null,
            queue: {
                pending: null,
                lanes: 0,
                dispatch: null,
                lastRenderedReducer: Kt,
                lastRenderedState: l
            },
            next: null
        }, e.memoizedState = t, e = e.alternate, e !== null && (e.memoizedState = t), t
    }

    function Ro(e) {
        var t = Oo(e);
        t.next === null && (t = e.alternate.memoizedState), un(e, t.next.queue, {}, bt())
    }

    function yc() {
        return We(Tn)
    }

    function Uo() {
        return Le().memoizedState
    }

    function Co() {
        return Le().memoizedState
    }

    function Th(e) {
        for (var t = e.return; t !== null;) {
            switch (t.tag) {
            case 24:
            case 3:
                var l = bt();
                e = rl(l);
                var a = dl(t, e, l);
                a !== null && (ft(a, t, l), en(a, t, l)), t = {
                    cache: Zi()
                }, e.payload = t;
                return
            }
            t = t.return
        }
    }

    function xh(e, t, l) {
        var a = bt();
        l = {
            lane: a,
            revertLane: 0,
            gesture: null,
            action: l,
            hasEagerState: !1,
            eagerState: null,
            next: null
        }, vu(e) ? qo(t, l) : (l = Hi(e, t, l, a), l !== null && (ft(l, e, a), Bo(l, t, a)))
    }

    function Ho(e, t, l) {
        var a = bt();
        un(e, t, l, a)
    }

    function un(e, t, l, a) {
        var n = {
            lane: a,
            revertLane: 0,
            gesture: null,
            action: l,
            hasEagerState: !1,
            eagerState: null,
            next: null
        };
        if (vu(e)) qo(t, n);
        else {
            var u = e.alternate;
            if (e.lanes === 0 && (u === null || u.lanes === 0) && (u = t.lastRenderedReducer, u !== null)) try {
                var i = t.lastRenderedState,
                    s = u(i, l);
                if (n.hasEagerState = !0, n.eagerState = s, ht(s, i)) return Wn(e, t, n, 0), xe === null && Jn(), !1
            } catch {}
            if (l = Hi(e, t, n, a), l !== null) return ft(l, e, a), Bo(l, t, a), !0
        }
        return !1
    }

    function pc(e, t, l, a) {
        if (a = {
                lane: 2,
                revertLane: $c(),
                gesture: null,
                action: a,
                hasEagerState: !1,
                eagerState: null,
                next: null
            }, vu(e)) {
            if (t) throw Error(o(479))
        } else t = Hi(e, l, a, 2), t !== null && ft(t, e, 2)
    }

    function vu(e) {
        var t = e.alternate;
        return e === te || t !== null && t === te
    }

    function qo(e, t) {
        ga = su = !0;
        var l = e.pending;
        l === null ? t.next = t : (t.next = l.next, l.next = t), e.pending = t
    }

    function Bo(e, t, l) {
        if ((l & 4194048) !== 0) {
            var a = t.lanes;
            a &= e.pendingLanes, l |= a, t.lanes = l, Ys(e, l)
        }
    }
    var cn = {
        readContext: We,
        use: ru,
        useCallback: Ce,
        useContext: Ce,
        useEffect: Ce,
        useImperativeHandle: Ce,
        useLayoutEffect: Ce,
        useInsertionEffect: Ce,
        useMemo: Ce,
        useReducer: Ce,
        useRef: Ce,
        useState: Ce,
        useDebugValue: Ce,
        useDeferredValue: Ce,
        useTransition: Ce,
        useSyncExternalStore: Ce,
        useId: Ce,
        useHostTransitionStatus: Ce,
        useFormState: Ce,
        useActionState: Ce,
        useOptimistic: Ce,
        useMemoCache: Ce,
        useCacheRefresh: Ce
    };
    cn.useEffectEvent = Ce;
    var Lo = {
            readContext: We,
            use: ru,
            useCallback: function (e, t) {
                return lt().memoizedState = [e, t === void 0 ? null : t], e
            },
            useContext: We,
            useEffect: No,
            useImperativeHandle: function (e, t, l) {
                l = l != null ? l.concat([e]) : null, mu(4194308, 4, zo.bind(null, t, e), l)
            },
            useLayoutEffect: function (e, t) {
                return mu(4194308, 4, e, t)
            },
            useInsertionEffect: function (e, t) {
                mu(4, 2, e, t)
            },
            useMemo: function (e, t) {
                var l = lt();
                t = t === void 0 ? null : t;
                var a = e();
                if (Ql) {
                    al(!0);
                    try {
                        e()
                    } finally {
                        al(!1)
                    }
                }
                return l.memoizedState = [a, t], a
            },
            useReducer: function (e, t, l) {
                var a = lt();
                if (l !== void 0) {
                    var n = l(t);
                    if (Ql) {
                        al(!0);
                        try {
                            l(t)
                        } finally {
                            al(!1)
                        }
                    }
                } else n = t;
                return a.memoizedState = a.baseState = n, e = {
                    pending: null,
                    lanes: 0,
                    dispatch: null,
                    lastRenderedReducer: e,
                    lastRenderedState: n
                }, a.queue = e, e = e.dispatch = xh.bind(null, te, e), [a.memoizedState, e]
            },
            useRef: function (e) {
                var t = lt();
                return e = {
                    current: e
                }, t.memoizedState = e
            },
            useState: function (e) {
                e = rc(e);
                var t = e.queue,
                    l = Ho.bind(null, te, t);
                return t.dispatch = l, [e.memoizedState, l]
            },
            useDebugValue: hc,
            useDeferredValue: function (e, t) {
                var l = lt();
                return vc(l, e, t)
            },
            useTransition: function () {
                var e = rc(!1);
                return e = _o.bind(null, te, e.queue, !0, !1), lt().memoizedState = e, [!1, e]
            },
            useSyncExternalStore: function (e, t, l) {
                var a = te,
                    n = lt();
                if (re) {
                    if (l === void 0) throw Error(o(407));
                    l = l()
                } else {
                    if (l = t(), xe === null) throw Error(o(349));
                    (fe & 127) !== 0 || no(a, t, l)
                }
                n.memoizedState = l;
                var u = {
                    value: l,
                    getSnapshot: t
                };
                return n.queue = u, No(io.bind(null, a, u, e), [e]), a.flags |= 2048, pa(9, {
                    destroy: void 0
                }, uo.bind(null, a, u, l, t), null), l
            },
            useId: function () {
                var e = lt(),
                    t = xe.identifierPrefix;
                if (re) {
                    var l = qt,
                        a = Ht;
                    l = (a & ~(1 << 32 - mt(a) - 1)).toString(32) + l, t = "_" + t + "R_" + l, l = fu++, 0 < l && (t += "H" + l.toString(32)), t += "_"
                } else l = yh++, t = "_" + t + "r_" + l.toString(32) + "_";
                return e.memoizedState = t
            },
            useHostTransitionStatus: yc,
            useFormState: go,
            useActionState: go,
            useOptimistic: function (e) {
                var t = lt();
                t.memoizedState = t.baseState = e;
                var l = {
                    pending: null,
                    lanes: 0,
                    dispatch: null,
                    lastRenderedReducer: null,
                    lastRenderedState: null
                };
                return t.queue = l, t = pc.bind(null, te, !0, l), l.dispatch = t, [e, t]
            },
            useMemoCache: sc,
            useCacheRefresh: function () {
                return lt().memoizedState = Th.bind(null, te)
            },
            useEffectEvent: function (e) {
                var t = lt(),
                    l = {
                        impl: e
                    };
                return t.memoizedState = l,
                    function () {
                        if ((he & 2) !== 0) throw Error(o(440));
                        return l.impl.apply(void 0, arguments)
                    }
            }
        },
        Sc = {
            readContext: We,
            use: ru,
            useCallback: Mo,
            useContext: We,
            useEffect: mc,
            useImperativeHandle: jo,
            useInsertionEffect: To,
            useLayoutEffect: xo,
            useMemo: Do,
            useReducer: du,
            useRef: bo,
            useState: function () {
                return du(Kt)
            },
            useDebugValue: hc,
            useDeferredValue: function (e, t) {
                var l = Le();
                return Ao(l, be.memoizedState, e, t)
            },
            useTransition: function () {
                var e = du(Kt)[0],
                    t = Le().memoizedState;
                return [typeof e == "boolean" ? e : nn(e), t]
            },
            useSyncExternalStore: ao,
            useId: Uo,
            useHostTransitionStatus: yc,
            useFormState: yo,
            useActionState: yo,
            useOptimistic: function (e, t) {
                var l = Le();
                return fo(l, be, e, t)
            },
            useMemoCache: sc,
            useCacheRefresh: Co
        };
    Sc.useEffectEvent = Eo;
    var ko = {
        readContext: We,
        use: ru,
        useCallback: Mo,
        useContext: We,
        useEffect: mc,
        useImperativeHandle: jo,
        useInsertionEffect: To,
        useLayoutEffect: xo,
        useMemo: Do,
        useReducer: oc,
        useRef: bo,
        useState: function () {
            return oc(Kt)
        },
        useDebugValue: hc,
        useDeferredValue: function (e, t) {
            var l = Le();
            return be === null ? vc(l, e, t) : Ao(l, be.memoizedState, e, t)
        },
        useTransition: function () {
            var e = oc(Kt)[0],
                t = Le().memoizedState;
            return [typeof e == "boolean" ? e : nn(e), t]
        },
        useSyncExternalStore: ao,
        useId: Uo,
        useHostTransitionStatus: yc,
        useFormState: So,
        useActionState: So,
        useOptimistic: function (e, t) {
            var l = Le();
            return be !== null ? fo(l, be, e, t) : (l.baseState = e, [e, l.queue.dispatch])
        },
        useMemoCache: sc,
        useCacheRefresh: Co
    };
    ko.useEffectEvent = Eo;

    function bc(e, t, l, a) {
        t = e.memoizedState, l = l(a, t), l = l == null ? t : M({}, t, l), e.memoizedState = l, e.lanes === 0 && (e.updateQueue.baseState = l)
    }
    var Nc = {
        enqueueSetState: function (e, t, l) {
            e = e._reactInternals;
            var a = bt(),
                n = rl(a);
            n.payload = t, l != null && (n.callback = l), t = dl(e, n, a), t !== null && (ft(t, e, a), en(t, e, a))
        },
        enqueueReplaceState: function (e, t, l) {
            e = e._reactInternals;
            var a = bt(),
                n = rl(a);
            n.tag = 1, n.payload = t, l != null && (n.callback = l), t = dl(e, n, a), t !== null && (ft(t, e, a), en(t, e, a))
        },
        enqueueForceUpdate: function (e, t) {
            e = e._reactInternals;
            var l = bt(),
                a = rl(l);
            a.tag = 2, t != null && (a.callback = t), t = dl(e, a, l), t !== null && (ft(t, e, l), en(t, e, l))
        }
    };

    function Yo(e, t, l, a, n, u, i) {
        return e = e.stateNode, typeof e.shouldComponentUpdate == "function" ? e.shouldComponentUpdate(a, u, i) : t.prototype && t.prototype.isPureReactComponent ? !Za(l, a) || !Za(n, u) : !0
    }

    function Go(e, t, l, a) {
        e = t.state, typeof t.componentWillReceiveProps == "function" && t.componentWillReceiveProps(l, a), typeof t.UNSAFE_componentWillReceiveProps == "function" && t.UNSAFE_componentWillReceiveProps(l, a), t.state !== e && Nc.enqueueReplaceState(t, t.state, null)
    }

    function Vl(e, t) {
        var l = t;
        if ("ref" in t) {
            l = {};
            for (var a in t) a !== "ref" && (l[a] = t[a])
        }
        if (e = e.defaultProps) {
            l === t && (l = M({}, l));
            for (var n in e) l[n] === void 0 && (l[n] = e[n])
        }
        return l
    }

    function Xo(e) {
        Kn(e)
    }

    function Qo(e) {
        console.error(e)
    }

    function Vo(e) {
        Kn(e)
    }

    function gu(e, t) {
        try {
            var l = e.onUncaughtError;
            l(t.value, {
                componentStack: t.stack
            })
        } catch (a) {
            setTimeout(function () {
                throw a
            })
        }
    }

    function wo(e, t, l) {
        try {
            var a = e.onCaughtError;
            a(l.value, {
                componentStack: l.stack,
                errorBoundary: t.tag === 1 ? t.stateNode : null
            })
        } catch (n) {
            setTimeout(function () {
                throw n
            })
        }
    }

    function Ec(e, t, l) {
        return l = rl(l), l.tag = 3, l.payload = {
            element: null
        }, l.callback = function () {
            gu(e, t)
        }, l
    }

    function Zo(e) {
        return e = rl(e), e.tag = 3, e
    }

    function Ko(e, t, l, a) {
        var n = l.type.getDerivedStateFromError;
        if (typeof n == "function") {
            var u = a.value;
            e.payload = function () {
                return n(u)
            }, e.callback = function () {
                wo(t, l, a)
            }
        }
        var i = l.stateNode;
        i !== null && typeof i.componentDidCatch == "function" && (e.callback = function () {
            wo(t, l, a), typeof n != "function" && (pl === null ? pl = new Set([this]) : pl.add(this));
            var s = a.stack;
            this.componentDidCatch(a.value, {
                componentStack: s !== null ? s : ""
            })
        })
    }

    function zh(e, t, l, a, n) {
        if (l.flags |= 32768, a !== null && typeof a == "object" && typeof a.then == "function") {
            if (t = l.alternate, t !== null && oa(t, l, n, !0), l = gt.current, l !== null) {
                switch (l.tag) {
                case 31:
                case 13:
                    return Dt === null ? Du() : l.alternate === null && He === 0 && (He = 3), l.flags &= -257, l.flags |= 65536, l.lanes = n, a === au ? l.flags |= 16384 : (t = l.updateQueue, t === null ? l.updateQueue = new Set([a]) : t.add(a), Kc(e, a, n)), !1;
                case 22:
                    return l.flags |= 65536, a === au ? l.flags |= 16384 : (t = l.updateQueue, t === null ? (t = {
                        transitions: null,
                        markerInstances: null,
                        retryQueue: new Set([a])
                    }, l.updateQueue = t) : (l = t.retryQueue, l === null ? t.retryQueue = new Set([a]) : l.add(a)), Kc(e, a, n)), !1
                }
                throw Error(o(435, l.tag))
            }
            return Kc(e, a, n), Du(), !1
        }
        if (re) return t = gt.current, t !== null ? ((t.flags & 65536) === 0 && (t.flags |= 256), t.flags |= 65536, t.lanes = n, a !== Gi && (e = Error(o(422), {
            cause: a
        }), Wa(xt(e, l)))) : (a !== Gi && (t = Error(o(423), {
            cause: a
        }), Wa(xt(t, l))), e = e.current.alternate, e.flags |= 65536, n &= -n, e.lanes |= n, a = xt(a, l), n = Ec(e.stateNode, a, n), Ii(e, n), He !== 4 && (He = 2)), !1;
        var u = Error(o(520), {
            cause: a
        });
        if (u = xt(u, l), vn === null ? vn = [u] : vn.push(u), He !== 4 && (He = 2), t === null) return !0;
        a = xt(a, l), l = t;
        do {
            switch (l.tag) {
            case 3:
                return l.flags |= 65536, e = n & -n, l.lanes |= e, e = Ec(l.stateNode, a, e), Ii(l, e), !1;
            case 1:
                if (t = l.type, u = l.stateNode, (l.flags & 128) === 0 && (typeof t.getDerivedStateFromError == "function" || u !== null && typeof u.componentDidCatch == "function" && (pl === null || !pl.has(u)))) return l.flags |= 65536, n &= -n, l.lanes |= n, n = Zo(n), Ko(n, e, l, a), Ii(l, n), !1
            }
            l = l.return
        } while (l !== null);
        return !1
    }
    var Tc = Error(o(461)),
        Ge = !1;

    function $e(e, t, l, a) {
        t.child = e === null ? $f(t, null, l, a) : Xl(t, e.child, l, a)
    }

    function Jo(e, t, l, a, n) {
        l = l.render;
        var u = t.ref;
        if ("ref" in a) {
            var i = {};
            for (var s in a) s !== "ref" && (i[s] = a[s])
        } else i = a;
        return Ll(t), a = nc(e, t, l, i, u, n), s = uc(), e !== null && !Ge ? (ic(e, t, n), Jt(e, t, n)) : (re && s && ki(t), t.flags |= 1, $e(e, t, a, n), t.child)
    }

    function Wo(e, t, l, a, n) {
        if (e === null) {
            var u = l.type;
            return typeof u == "function" && !qi(u) && u.defaultProps === void 0 && l.compare === null ? (t.tag = 15, t.type = u, $o(e, t, u, a, n)) : (e = Fn(l.type, null, a, t, t.mode, n), e.ref = t.ref, e.return = t, t.child = e)
        }
        if (u = e.child, !Oc(e, n)) {
            var i = u.memoizedProps;
            if (l = l.compare, l = l !== null ? l : Za, l(i, a) && e.ref === t.ref) return Jt(e, t, n)
        }
        return t.flags |= 1, e = Xt(u, a), e.ref = t.ref, e.return = t, t.child = e
    }

    function $o(e, t, l, a, n) {
        if (e !== null) {
            var u = e.memoizedProps;
            if (Za(u, a) && e.ref === t.ref)
                if (Ge = !1, t.pendingProps = a = u, Oc(e, n))(e.flags & 131072) !== 0 && (Ge = !0);
                else return t.lanes = e.lanes, Jt(e, t, n)
        }
        return xc(e, t, l, a, n)
    }

    function Fo(e, t, l, a) {
        var n = a.children,
            u = e !== null ? e.memoizedState : null;
        if (e === null && t.stateNode === null && (t.stateNode = {
                _visibility: 1,
                _pendingMarkers: null,
                _retryCache: null,
                _transitions: null
            }), a.mode === "hidden") {
            if ((t.flags & 128) !== 0) {
                if (u = u !== null ? u.baseLanes | l : l, e !== null) {
                    for (a = t.child = e.child, n = 0; a !== null;) n = n | a.lanes | a.childLanes, a = a.sibling;
                    a = n & ~u
                } else a = 0, t.child = null;
                return Io(e, t, u, l, a)
            }
            if ((l & 536870912) !== 0) t.memoizedState = {
                baseLanes: 0,
                cachePool: null
            }, e !== null && tu(t, u !== null ? u.cachePool : null), u !== null ? Pf(t, u) : ec(), eo(t);
            else return a = t.lanes = 536870912, Io(e, t, u !== null ? u.baseLanes | l : l, l, a)
        } else u !== null ? (tu(t, u.cachePool), Pf(t, u), hl(), t.memoizedState = null) : (e !== null && tu(t, null), ec(), hl());
        return $e(e, t, n, l), t.child
    }

    function sn(e, t) {
        return e !== null && e.tag === 22 || t.stateNode !== null || (t.stateNode = {
            _visibility: 1,
            _pendingMarkers: null,
            _retryCache: null,
            _transitions: null
        }), t.sibling
    }

    function Io(e, t, l, a, n) {
        var u = Ji();
        return u = u === null ? null : {
            parent: ke._currentValue,
            pool: u
        }, t.memoizedState = {
            baseLanes: l,
            cachePool: u
        }, e !== null && tu(t, null), ec(), eo(t), e !== null && oa(e, t, a, !0), t.childLanes = n, null
    }

    function yu(e, t) {
        return t = Su({
            mode: t.mode,
            children: t.children
        }, e.mode), t.ref = e.ref, e.child = t, t.return = e, t
    }

    function Po(e, t, l) {
        return Xl(t, e.child, null, l), e = yu(t, t.pendingProps), e.flags |= 2, yt(t), t.memoizedState = null, e
    }

    function jh(e, t, l) {
        var a = t.pendingProps,
            n = (t.flags & 128) !== 0;
        if (t.flags &= -129, e === null) {
            if (re) {
                if (a.mode === "hidden") return e = yu(t, a), t.lanes = 536870912, sn(null, e);
                if (lc(t), (e = Ae) ? (e = rd(e, Mt), e = e !== null && e.data === "&" ? e : null, e !== null && (t.memoizedState = {
                        dehydrated: e,
                        treeContext: il !== null ? {
                            id: Ht,
                            overflow: qt
                        } : null,
                        retryLane: 536870912,
                        hydrationErrors: null
                    }, l = Hf(e), l.return = t, t.child = l, Je = t, Ae = null)) : e = null, e === null) throw sl(t);
                return t.lanes = 536870912, null
            }
            return yu(t, a)
        }
        var u = e.memoizedState;
        if (u !== null) {
            var i = u.dehydrated;
            if (lc(t), n)
                if (t.flags & 256) t.flags &= -257, t = Po(e, t, l);
                else if (t.memoizedState !== null) t.child = e.child, t.flags |= 128, t = null;
            else throw Error(o(558));
            else if (Ge || oa(e, t, l, !1), n = (l & e.childLanes) !== 0, Ge || n) {
                if (a = xe, a !== null && (i = Gs(a, l), i !== 0 && i !== u.retryLane)) throw u.retryLane = i, Cl(e, i), ft(a, e, i), Tc;
                Du(), t = Po(e, t, l)
            } else e = u.treeContext, Ae = At(i.nextSibling), Je = t, re = !0, cl = null, Mt = !1, e !== null && Lf(t, e), t = yu(t, a), t.flags |= 4096;
            return t
        }
        return e = Xt(e.child, {
            mode: a.mode,
            children: a.children
        }), e.ref = t.ref, t.child = e, e.return = t, e
    }

    function pu(e, t) {
        var l = t.ref;
        if (l === null) e !== null && e.ref !== null && (t.flags |= 4194816);
        else {
            if (typeof l != "function" && typeof l != "object") throw Error(o(284));
            (e === null || e.ref !== l) && (t.flags |= 4194816)
        }
    }

    function xc(e, t, l, a, n) {
        return Ll(t), l = nc(e, t, l, a, void 0, n), a = uc(), e !== null && !Ge ? (ic(e, t, n), Jt(e, t, n)) : (re && a && ki(t), t.flags |= 1, $e(e, t, l, n), t.child)
    }

    function er(e, t, l, a, n, u) {
        return Ll(t), t.updateQueue = null, l = lo(t, a, l, n), to(e), a = uc(), e !== null && !Ge ? (ic(e, t, u), Jt(e, t, u)) : (re && a && ki(t), t.flags |= 1, $e(e, t, l, u), t.child)
    }

    function tr(e, t, l, a, n) {
        if (Ll(t), t.stateNode === null) {
            var u = ia,
                i = l.contextType;
            typeof i == "object" && i !== null && (u = We(i)), u = new l(a, u), t.memoizedState = u.state !== null && u.state !== void 0 ? u.state : null, u.updater = Nc, t.stateNode = u, u._reactInternals = t, u = t.stateNode, u.props = a, u.state = t.memoizedState, u.refs = {}, $i(t), i = l.contextType, u.context = typeof i == "object" && i !== null ? We(i) : ia, u.state = t.memoizedState, i = l.getDerivedStateFromProps, typeof i == "function" && (bc(t, l, i, a), u.state = t.memoizedState), typeof l.getDerivedStateFromProps == "function" || typeof u.getSnapshotBeforeUpdate == "function" || typeof u.UNSAFE_componentWillMount != "function" && typeof u.componentWillMount != "function" || (i = u.state, typeof u.componentWillMount == "function" && u.componentWillMount(), typeof u.UNSAFE_componentWillMount == "function" && u.UNSAFE_componentWillMount(), i !== u.state && Nc.enqueueReplaceState(u, u.state, null), ln(t, a, u, n), tn(), u.state = t.memoizedState), typeof u.componentDidMount == "function" && (t.flags |= 4194308), a = !0
        } else if (e === null) {
            u = t.stateNode;
            var s = t.memoizedProps,
                r = Vl(l, s);
            u.props = r;
            var y = u.context,
                T = l.contextType;
            i = ia, typeof T == "object" && T !== null && (i = We(T));
            var D = l.getDerivedStateFromProps;
            T = typeof D == "function" || typeof u.getSnapshotBeforeUpdate == "function", s = t.pendingProps !== s, T || typeof u.UNSAFE_componentWillReceiveProps != "function" && typeof u.componentWillReceiveProps != "function" || (s || y !== i) && Go(t, u, a, i), ol = !1;
            var p = t.memoizedState;
            u.state = p, ln(t, a, u, n), tn(), y = t.memoizedState, s || p !== y || ol ? (typeof D == "function" && (bc(t, l, D, a), y = t.memoizedState), (r = ol || Yo(t, l, r, a, p, y, i)) ? (T || typeof u.UNSAFE_componentWillMount != "function" && typeof u.componentWillMount != "function" || (typeof u.componentWillMount == "function" && u.componentWillMount(), typeof u.UNSAFE_componentWillMount == "function" && u.UNSAFE_componentWillMount()), typeof u.componentDidMount == "function" && (t.flags |= 4194308)) : (typeof u.componentDidMount == "function" && (t.flags |= 4194308), t.memoizedProps = a, t.memoizedState = y), u.props = a, u.state = y, u.context = i, a = r) : (typeof u.componentDidMount == "function" && (t.flags |= 4194308), a = !1)
        } else {
            u = t.stateNode, Fi(e, t), i = t.memoizedProps, T = Vl(l, i), u.props = T, D = t.pendingProps, p = u.context, y = l.contextType, r = ia, typeof y == "object" && y !== null && (r = We(y)), s = l.getDerivedStateFromProps, (y = typeof s == "function" || typeof u.getSnapshotBeforeUpdate == "function") || typeof u.UNSAFE_componentWillReceiveProps != "function" && typeof u.componentWillReceiveProps != "function" || (i !== D || p !== r) && Go(t, u, a, r), ol = !1, p = t.memoizedState, u.state = p, ln(t, a, u, n), tn();
            var E = t.memoizedState;
            i !== D || p !== E || ol || e !== null && e.dependencies !== null && Pn(e.dependencies) ? (typeof s == "function" && (bc(t, l, s, a), E = t.memoizedState), (T = ol || Yo(t, l, T, a, p, E, r) || e !== null && e.dependencies !== null && Pn(e.dependencies)) ? (y || typeof u.UNSAFE_componentWillUpdate != "function" && typeof u.componentWillUpdate != "function" || (typeof u.componentWillUpdate == "function" && u.componentWillUpdate(a, E, r), typeof u.UNSAFE_componentWillUpdate == "function" && u.UNSAFE_componentWillUpdate(a, E, r)), typeof u.componentDidUpdate == "function" && (t.flags |= 4), typeof u.getSnapshotBeforeUpdate == "function" && (t.flags |= 1024)) : (typeof u.componentDidUpdate != "function" || i === e.memoizedProps && p === e.memoizedState || (t.flags |= 4), typeof u.getSnapshotBeforeUpdate != "function" || i === e.memoizedProps && p === e.memoizedState || (t.flags |= 1024), t.memoizedProps = a, t.memoizedState = E), u.props = a, u.state = E, u.context = r, a = T) : (typeof u.componentDidUpdate != "function" || i === e.memoizedProps && p === e.memoizedState || (t.flags |= 4), typeof u.getSnapshotBeforeUpdate != "function" || i === e.memoizedProps && p === e.memoizedState || (t.flags |= 1024), a = !1)
        }
        return u = a, pu(e, t), a = (t.flags & 128) !== 0, u || a ? (u = t.stateNode, l = a && typeof l.getDerivedStateFromError != "function" ? null : u.render(), t.flags |= 1, e !== null && a ? (t.child = Xl(t, e.child, null, n), t.child = Xl(t, null, l, n)) : $e(e, t, l, n), t.memoizedState = u.state, e = t.child) : e = Jt(e, t, n), e
    }

    function lr(e, t, l, a) {
        return ql(), t.flags |= 256, $e(e, t, l, a), t.child
    }
    var zc = {
        dehydrated: null,
        treeContext: null,
        retryLane: 0,
        hydrationErrors: null
    };

    function jc(e) {
        return {
            baseLanes: e,
            cachePool: Vf()
        }
    }

    function Mc(e, t, l) {
        return e = e !== null ? e.childLanes & ~l : 0, t && (e |= St), e
    }

    function ar(e, t, l) {
        var a = t.pendingProps,
            n = !1,
            u = (t.flags & 128) !== 0,
            i;
        if ((i = u) || (i = e !== null && e.memoizedState === null ? !1 : (Be.current & 2) !== 0), i && (n = !0, t.flags &= -129), i = (t.flags & 32) !== 0, t.flags &= -33, e === null) {
            if (re) {
                if (n ? ml(t) : hl(), (e = Ae) ? (e = rd(e, Mt), e = e !== null && e.data !== "&" ? e : null, e !== null && (t.memoizedState = {
                        dehydrated: e,
                        treeContext: il !== null ? {
                            id: Ht,
                            overflow: qt
                        } : null,
                        retryLane: 536870912,
                        hydrationErrors: null
                    }, l = Hf(e), l.return = t, t.child = l, Je = t, Ae = null)) : e = null, e === null) throw sl(t);
                return fs(e) ? t.lanes = 32 : t.lanes = 536870912, null
            }
            var s = a.children;
            return a = a.fallback, n ? (hl(), n = t.mode, s = Su({
                mode: "hidden",
                children: s
            }, n), a = Hl(a, n, l, null), s.return = t, a.return = t, s.sibling = a, t.child = s, a = t.child, a.memoizedState = jc(l), a.childLanes = Mc(e, i, l), t.memoizedState = zc, sn(null, a)) : (ml(t), Dc(t, s))
        }
        var r = e.memoizedState;
        if (r !== null && (s = r.dehydrated, s !== null)) {
            if (u) t.flags & 256 ? (ml(t), t.flags &= -257, t = Ac(e, t, l)) : t.memoizedState !== null ? (hl(), t.child = e.child, t.flags |= 128, t = null) : (hl(), s = a.fallback, n = t.mode, a = Su({
                mode: "visible",
                children: a.children
            }, n), s = Hl(s, n, l, null), s.flags |= 2, a.return = t, s.return = t, a.sibling = s, t.child = a, Xl(t, e.child, null, l), a = t.child, a.memoizedState = jc(l), a.childLanes = Mc(e, i, l), t.memoizedState = zc, t = sn(null, a));
            else if (ml(t), fs(s)) {
                if (i = s.nextSibling && s.nextSibling.dataset, i) var y = i.dgst;
                i = y, a = Error(o(419)), a.stack = "", a.digest = i, Wa({
                    value: a,
                    source: null,
                    stack: null
                }), t = Ac(e, t, l)
            } else if (Ge || oa(e, t, l, !1), i = (l & e.childLanes) !== 0, Ge || i) {
                if (i = xe, i !== null && (a = Gs(i, l), a !== 0 && a !== r.retryLane)) throw r.retryLane = a, Cl(e, a), ft(i, e, a), Tc;
                ss(s) || Du(), t = Ac(e, t, l)
            } else ss(s) ? (t.flags |= 192, t.child = e.child, t = null) : (e = r.treeContext, Ae = At(s.nextSibling), Je = t, re = !0, cl = null, Mt = !1, e !== null && Lf(t, e), t = Dc(t, a.children), t.flags |= 4096);
            return t
        }
        return n ? (hl(), s = a.fallback, n = t.mode, r = e.child, y = r.sibling, a = Xt(r, {
            mode: "hidden",
            children: a.children
        }), a.subtreeFlags = r.subtreeFlags & 65011712, y !== null ? s = Xt(y, s) : (s = Hl(s, n, l, null), s.flags |= 2), s.return = t, a.return = t, a.sibling = s, t.child = a, sn(null, a), a = t.child, s = e.child.memoizedState, s === null ? s = jc(l) : (n = s.cachePool, n !== null ? (r = ke._currentValue, n = n.parent !== r ? {
            parent: r,
            pool: r
        } : n) : n = Vf(), s = {
            baseLanes: s.baseLanes | l,
            cachePool: n
        }), a.memoizedState = s, a.childLanes = Mc(e, i, l), t.memoizedState = zc, sn(e.child, a)) : (ml(t), l = e.child, e = l.sibling, l = Xt(l, {
            mode: "visible",
            children: a.children
        }), l.return = t, l.sibling = null, e !== null && (i = t.deletions, i === null ? (t.deletions = [e], t.flags |= 16) : i.push(e)), t.child = l, t.memoizedState = null, l)
    }

    function Dc(e, t) {
        return t = Su({
            mode: "visible",
            children: t
        }, e.mode), t.return = e, e.child = t
    }

    function Su(e, t) {
        return e = vt(22, e, null, t), e.lanes = 0, e
    }

    function Ac(e, t, l) {
        return Xl(t, e.child, null, l), e = Dc(t, t.pendingProps.children), e.flags |= 2, t.memoizedState = null, e
    }

    function nr(e, t, l) {
        e.lanes |= t;
        var a = e.alternate;
        a !== null && (a.lanes |= t), Vi(e.return, t, l)
    }

    function _c(e, t, l, a, n, u) {
        var i = e.memoizedState;
        i === null ? e.memoizedState = {
            isBackwards: t,
            rendering: null,
            renderingStartTime: 0,
            last: a,
            tail: l,
            tailMode: n,
            treeForkCount: u
        } : (i.isBackwards = t, i.rendering = null, i.renderingStartTime = 0, i.last = a, i.tail = l, i.tailMode = n, i.treeForkCount = u)
    }

    function ur(e, t, l) {
        var a = t.pendingProps,
            n = a.revealOrder,
            u = a.tail;
        a = a.children;
        var i = Be.current,
            s = (i & 2) !== 0;
        if (s ? (i = i & 1 | 2, t.flags |= 128) : i &= 1, B(Be, i), $e(e, t, a, l), a = re ? Ja : 0, !s && e !== null && (e.flags & 128) !== 0) e: for (e = t.child; e !== null;) {
            if (e.tag === 13) e.memoizedState !== null && nr(e, l, t);
            else if (e.tag === 19) nr(e, l, t);
            else if (e.child !== null) {
                e.child.return = e, e = e.child;
                continue
            }
            if (e === t) break e;
            for (; e.sibling === null;) {
                if (e.return === null || e.return === t) break e;
                e = e.return
            }
            e.sibling.return = e.return, e = e.sibling
        }
        switch (n) {
        case "forwards":
            for (l = t.child, n = null; l !== null;) e = l.alternate, e !== null && cu(e) === null && (n = l), l = l.sibling;
            l = n, l === null ? (n = t.child, t.child = null) : (n = l.sibling, l.sibling = null), _c(t, !1, n, l, u, a);
            break;
        case "backwards":
        case "unstable_legacy-backwards":
            for (l = null, n = t.child, t.child = null; n !== null;) {
                if (e = n.alternate, e !== null && cu(e) === null) {
                    t.child = n;
                    break
                }
                e = n.sibling, n.sibling = l, l = n, n = e
            }
            _c(t, !0, l, null, u, a);
            break;
        case "together":
            _c(t, !1, null, null, void 0, a);
            break;
        default:
            t.memoizedState = null
        }
        return t.child
    }

    function Jt(e, t, l) {
        if (e !== null && (t.dependencies = e.dependencies), yl |= t.lanes, (l & t.childLanes) === 0)
            if (e !== null) {
                if (oa(e, t, l, !1), (l & t.childLanes) === 0) return null
            } else return null;
        if (e !== null && t.child !== e.child) throw Error(o(153));
        if (t.child !== null) {
            for (e = t.child, l = Xt(e, e.pendingProps), t.child = l, l.return = t; e.sibling !== null;) e = e.sibling, l = l.sibling = Xt(e, e.pendingProps), l.return = t;
            l.sibling = null
        }
        return t.child
    }

    function Oc(e, t) {
        return (e.lanes & t) !== 0 ? !0 : (e = e.dependencies, !!(e !== null && Pn(e)))
    }

    function Mh(e, t, l) {
        switch (t.tag) {
        case 3:
            tt(t, t.stateNode.containerInfo), fl(t, ke, e.memoizedState.cache), ql();
            break;
        case 27:
        case 5:
            Ua(t);
            break;
        case 4:
            tt(t, t.stateNode.containerInfo);
            break;
        case 10:
            fl(t, t.type, t.memoizedProps.value);
            break;
        case 31:
            if (t.memoizedState !== null) return t.flags |= 128, lc(t), null;
            break;
        case 13:
            var a = t.memoizedState;
            if (a !== null) return a.dehydrated !== null ? (ml(t), t.flags |= 128, null) : (l & t.child.childLanes) !== 0 ? ar(e, t, l) : (ml(t), e = Jt(e, t, l), e !== null ? e.sibling : null);
            ml(t);
            break;
        case 19:
            var n = (e.flags & 128) !== 0;
            if (a = (l & t.childLanes) !== 0, a || (oa(e, t, l, !1), a = (l & t.childLanes) !== 0), n) {
                if (a) return ur(e, t, l);
                t.flags |= 128
            }
            if (n = t.memoizedState, n !== null && (n.rendering = null, n.tail = null, n.lastEffect = null), B(Be, Be.current), a) break;
            return null;
        case 22:
            return t.lanes = 0, Fo(e, t, l, t.pendingProps);
        case 24:
            fl(t, ke, e.memoizedState.cache)
        }
        return Jt(e, t, l)
    }

    function ir(e, t, l) {
        if (e !== null)
            if (e.memoizedProps !== t.pendingProps) Ge = !0;
            else {
                if (!Oc(e, l) && (t.flags & 128) === 0) return Ge = !1, Mh(e, t, l);
                Ge = (e.flags & 131072) !== 0
            }
        else Ge = !1, re && (t.flags & 1048576) !== 0 && Bf(t, Ja, t.index);
        switch (t.lanes = 0, t.tag) {
        case 16:
            e: {
                var a = t.pendingProps;
                if (e = Yl(t.elementType), t.type = e, typeof e == "function") qi(e) ? (a = Vl(e, a), t.tag = 1, t = tr(null, t, e, a, l)) : (t.tag = 0, t = xc(null, t, e, a, l));
                else {
                    if (e != null) {
                        var n = e.$$typeof;
                        if (n === Re) {
                            t.tag = 11, t = Jo(null, t, e, a, l);
                            break e
                        } else if (n === O) {
                            t.tag = 14, t = Wo(null, t, e, a, l);
                            break e
                        }
                    }
                    throw t = Ze(e) || e, Error(o(306, t, ""))
                }
            }
            return t;
        case 0:
            return xc(e, t, t.type, t.pendingProps, l);
        case 1:
            return a = t.type, n = Vl(a, t.pendingProps), tr(e, t, a, n, l);
        case 3:
            e: {
                if (tt(t, t.stateNode.containerInfo), e === null) throw Error(o(387));a = t.pendingProps;
                var u = t.memoizedState;n = u.element,
                Fi(e, t),
                ln(t, a, null, l);
                var i = t.memoizedState;
                if (a = i.cache, fl(t, ke, a), a !== u.cache && wi(t, [ke], l, !0), tn(), a = i.element, u.isDehydrated)
                    if (u = {
                            element: a,
                            isDehydrated: !1,
                            cache: i.cache
                        }, t.updateQueue.baseState = u, t.memoizedState = u, t.flags & 256) {
                        t = lr(e, t, a, l);
                        break e
                    } else if (a !== n) {
                    n = xt(Error(o(424)), t), Wa(n), t = lr(e, t, a, l);
                    break e
                } else
                    for (e = t.stateNode.containerInfo, e.nodeType === 9 ? e = e.body : e = e.nodeName === "HTML" ? e.ownerDocument.body : e, Ae = At(e.firstChild), Je = t, re = !0, cl = null, Mt = !0, l = $f(t, null, a, l), t.child = l; l;) l.flags = l.flags & -3 | 4096, l = l.sibling;
                else {
                    if (ql(), a === n) {
                        t = Jt(e, t, l);
                        break e
                    }
                    $e(e, t, a, l)
                }
                t = t.child
            }
            return t;
        case 26:
            return pu(e, t), e === null ? (l = yd(t.type, null, t.pendingProps, null)) ? t.memoizedState = l : re || (l = t.type, e = t.pendingProps, a = Hu(ue.current).createElement(l), a[Ke] = t, a[at] = e, Fe(a, l, e), Ve(a), t.stateNode = a) : t.memoizedState = yd(t.type, e.memoizedProps, t.pendingProps, e.memoizedState), null;
        case 27:
            return Ua(t), e === null && re && (a = t.stateNode = hd(t.type, t.pendingProps, ue.current), Je = t, Mt = !0, n = Ae, El(t.type) ? (os = n, Ae = At(a.firstChild)) : Ae = n), $e(e, t, t.pendingProps.children, l), pu(e, t), e === null && (t.flags |= 4194304), t.child;
        case 5:
            return e === null && re && ((n = a = Ae) && (a = a1(a, t.type, t.pendingProps, Mt), a !== null ? (t.stateNode = a, Je = t, Ae = At(a.firstChild), Mt = !1, n = !0) : n = !1), n || sl(t)), Ua(t), n = t.type, u = t.pendingProps, i = e !== null ? e.memoizedProps : null, a = u.children, us(n, u) ? a = null : i !== null && us(n, i) && (t.flags |= 32), t.memoizedState !== null && (n = nc(e, t, ph, null, null, l), Tn._currentValue = n), pu(e, t), $e(e, t, a, l), t.child;
        case 6:
            return e === null && re && ((e = l = Ae) && (l = n1(l, t.pendingProps, Mt), l !== null ? (t.stateNode = l, Je = t, Ae = null, e = !0) : e = !1), e || sl(t)), null;
        case 13:
            return ar(e, t, l);
        case 4:
            return tt(t, t.stateNode.containerInfo), a = t.pendingProps, e === null ? t.child = Xl(t, null, a, l) : $e(e, t, a, l), t.child;
        case 11:
            return Jo(e, t, t.type, t.pendingProps, l);
        case 7:
            return $e(e, t, t.pendingProps, l), t.child;
        case 8:
            return $e(e, t, t.pendingProps.children, l), t.child;
        case 12:
            return $e(e, t, t.pendingProps.children, l), t.child;
        case 10:
            return a = t.pendingProps, fl(t, t.type, a.value), $e(e, t, a.children, l), t.child;
        case 9:
            return n = t.type._context, a = t.pendingProps.children, Ll(t), n = We(n), a = a(n), t.flags |= 1, $e(e, t, a, l), t.child;
        case 14:
            return Wo(e, t, t.type, t.pendingProps, l);
        case 15:
            return $o(e, t, t.type, t.pendingProps, l);
        case 19:
            return ur(e, t, l);
        case 31:
            return jh(e, t, l);
        case 22:
            return Fo(e, t, l, t.pendingProps);
        case 24:
            return Ll(t), a = We(ke), e === null ? (n = Ji(), n === null && (n = xe, u = Zi(), n.pooledCache = u, u.refCount++, u !== null && (n.pooledCacheLanes |= l), n = u), t.memoizedState = {
                parent: a,
                cache: n
            }, $i(t), fl(t, ke, n)) : ((e.lanes & l) !== 0 && (Fi(e, t), ln(t, null, null, l), tn()), n = e.memoizedState, u = t.memoizedState, n.parent !== a ? (n = {
                parent: a,
                cache: a
            }, t.memoizedState = n, t.lanes === 0 && (t.memoizedState = t.updateQueue.baseState = n), fl(t, ke, a)) : (a = u.cache, fl(t, ke, a), a !== n.cache && wi(t, [ke], l, !0))), $e(e, t, t.pendingProps.children, l), t.child;
        case 29:
            throw t.pendingProps
        }
        throw Error(o(156, t.tag))
    }

    function Wt(e) {
        e.flags |= 4
    }

    function Rc(e, t, l, a, n) {
        if ((t = (e.mode & 32) !== 0) && (t = !1), t) {
            if (e.flags |= 16777216, (n & 335544128) === n)
                if (e.stateNode.complete) e.flags |= 8192;
                else if (Ur()) e.flags |= 8192;
            else throw Gl = au, Wi
        } else e.flags &= -16777217
    }

    function cr(e, t) {
        if (t.type !== "stylesheet" || (t.state.loading & 4) !== 0) e.flags &= -16777217;
        else if (e.flags |= 16777216, !Ed(t))
            if (Ur()) e.flags |= 8192;
            else throw Gl = au, Wi
    }

    function bu(e, t) {
        t !== null && (e.flags |= 4), e.flags & 16384 && (t = e.tag !== 22 ? Ls() : 536870912, e.lanes |= t, Ea |= t)
    }

    function fn(e, t) {
        if (!re) switch (e.tailMode) {
        case "hidden":
            t = e.tail;
            for (var l = null; t !== null;) t.alternate !== null && (l = t), t = t.sibling;
            l === null ? e.tail = null : l.sibling = null;
            break;
        case "collapsed":
            l = e.tail;
            for (var a = null; l !== null;) l.alternate !== null && (a = l), l = l.sibling;
            a === null ? t || e.tail === null ? e.tail = null : e.tail.sibling = null : a.sibling = null
        }
    }

    function _e(e) {
        var t = e.alternate !== null && e.alternate.child === e.child,
            l = 0,
            a = 0;
        if (t)
            for (var n = e.child; n !== null;) l |= n.lanes | n.childLanes, a |= n.subtreeFlags & 65011712, a |= n.flags & 65011712, n.return = e, n = n.sibling;
        else
            for (n = e.child; n !== null;) l |= n.lanes | n.childLanes, a |= n.subtreeFlags, a |= n.flags, n.return = e, n = n.sibling;
        return e.subtreeFlags |= a, e.childLanes = l, t
    }

    function Dh(e, t, l) {
        var a = t.pendingProps;
        switch (Yi(t), t.tag) {
        case 16:
        case 15:
        case 0:
        case 11:
        case 7:
        case 8:
        case 12:
        case 9:
        case 14:
            return _e(t), null;
        case 1:
            return _e(t), null;
        case 3:
            return l = t.stateNode, a = null, e !== null && (a = e.memoizedState.cache), t.memoizedState.cache !== a && (t.flags |= 2048), wt(ke), qe(), l.pendingContext && (l.context = l.pendingContext, l.pendingContext = null), (e === null || e.child === null) && (fa(t) ? Wt(t) : e === null || e.memoizedState.isDehydrated && (t.flags & 256) === 0 || (t.flags |= 1024, Xi())), _e(t), null;
        case 26:
            var n = t.type,
                u = t.memoizedState;
            return e === null ? (Wt(t), u !== null ? (_e(t), cr(t, u)) : (_e(t), Rc(t, n, null, a, l))) : u ? u !== e.memoizedState ? (Wt(t), _e(t), cr(t, u)) : (_e(t), t.flags &= -16777217) : (e = e.memoizedProps, e !== a && Wt(t), _e(t), Rc(t, n, e, a, l)), null;
        case 27:
            if (On(t), l = ue.current, n = t.type, e !== null && t.stateNode != null) e.memoizedProps !== a && Wt(t);
            else {
                if (!a) {
                    if (t.stateNode === null) throw Error(o(166));
                    return _e(t), null
                }
                e = Y.current, fa(t) ? kf(t) : (e = hd(n, a, l), t.stateNode = e, Wt(t))
            }
            return _e(t), null;
        case 5:
            if (On(t), n = t.type, e !== null && t.stateNode != null) e.memoizedProps !== a && Wt(t);
            else {
                if (!a) {
                    if (t.stateNode === null) throw Error(o(166));
                    return _e(t), null
                }
                if (u = Y.current, fa(t)) kf(t);
                else {
                    var i = Hu(ue.current);
                    switch (u) {
                    case 1:
                        u = i.createElementNS("http://www.w3.org/2000/svg", n);
                        break;
                    case 2:
                        u = i.createElementNS("http://www.w3.org/1998/Math/MathML", n);
                        break;
                    default:
                        switch (n) {
                        case "svg":
                            u = i.createElementNS("http://www.w3.org/2000/svg", n);
                            break;
                        case "math":
                            u = i.createElementNS("http://www.w3.org/1998/Math/MathML", n);
                            break;
                        case "script":
                            u = i.createElement("div"), u.innerHTML = "<script><\/script>", u = u.removeChild(u.firstChild);
                            break;
                        case "select":
                            u = typeof a.is == "string" ? i.createElement("select", {
                                is: a.is
                            }) : i.createElement("select"), a.multiple ? u.multiple = !0 : a.size && (u.size = a.size);
                            break;
                        default:
                            u = typeof a.is == "string" ? i.createElement(n, {
                                is: a.is
                            }) : i.createElement(n)
                        }
                    }
                    u[Ke] = t, u[at] = a;
                    e: for (i = t.child; i !== null;) {
                        if (i.tag === 5 || i.tag === 6) u.appendChild(i.stateNode);
                        else if (i.tag !== 4 && i.tag !== 27 && i.child !== null) {
                            i.child.return = i, i = i.child;
                            continue
                        }
                        if (i === t) break e;
                        for (; i.sibling === null;) {
                            if (i.return === null || i.return === t) break e;
                            i = i.return
                        }
                        i.sibling.return = i.return, i = i.sibling
                    }
                    t.stateNode = u;
                    e: switch (Fe(u, n, a), n) {
                    case "button":
                    case "input":
                    case "select":
                    case "textarea":
                        a = !!a.autoFocus;
                        break e;
                    case "img":
                        a = !0;
                        break e;
                    default:
                        a = !1
                    }
                    a && Wt(t)
                }
            }
            return _e(t), Rc(t, t.type, e === null ? null : e.memoizedProps, t.pendingProps, l), null;
        case 6:
            if (e && t.stateNode != null) e.memoizedProps !== a && Wt(t);
            else {
                if (typeof a != "string" && t.stateNode === null) throw Error(o(166));
                if (e = ue.current, fa(t)) {
                    if (e = t.stateNode, l = t.memoizedProps, a = null, n = Je, n !== null) switch (n.tag) {
                    case 27:
                    case 5:
                        a = n.memoizedProps
                    }
                    e[Ke] = t, e = !!(e.nodeValue === l || a !== null && a.suppressHydrationWarning === !0 || ad(e.nodeValue, l)), e || sl(t, !0)
                } else e = Hu(e).createTextNode(a), e[Ke] = t, t.stateNode = e
            }
            return _e(t), null;
        case 31:
            if (l = t.memoizedState, e === null || e.memoizedState !== null) {
                if (a = fa(t), l !== null) {
                    if (e === null) {
                        if (!a) throw Error(o(318));
                        if (e = t.memoizedState, e = e !== null ? e.dehydrated : null, !e) throw Error(o(557));
                        e[Ke] = t
                    } else ql(), (t.flags & 128) === 0 && (t.memoizedState = null), t.flags |= 4;
                    _e(t), e = !1
                } else l = Xi(), e !== null && e.memoizedState !== null && (e.memoizedState.hydrationErrors = l), e = !0;
                if (!e) return t.flags & 256 ? (yt(t), t) : (yt(t), null);
                if ((t.flags & 128) !== 0) throw Error(o(558))
            }
            return _e(t), null;
        case 13:
            if (a = t.memoizedState, e === null || e.memoizedState !== null && e.memoizedState.dehydrated !== null) {
                if (n = fa(t), a !== null && a.dehydrated !== null) {
                    if (e === null) {
                        if (!n) throw Error(o(318));
                        if (n = t.memoizedState, n = n !== null ? n.dehydrated : null, !n) throw Error(o(317));
                        n[Ke] = t
                    } else ql(), (t.flags & 128) === 0 && (t.memoizedState = null), t.flags |= 4;
                    _e(t), n = !1
                } else n = Xi(), e !== null && e.memoizedState !== null && (e.memoizedState.hydrationErrors = n), n = !0;
                if (!n) return t.flags & 256 ? (yt(t), t) : (yt(t), null)
            }
            return yt(t), (t.flags & 128) !== 0 ? (t.lanes = l, t) : (l = a !== null, e = e !== null && e.memoizedState !== null, l && (a = t.child, n = null, a.alternate !== null && a.alternate.memoizedState !== null && a.alternate.memoizedState.cachePool !== null && (n = a.alternate.memoizedState.cachePool.pool), u = null, a.memoizedState !== null && a.memoizedState.cachePool !== null && (u = a.memoizedState.cachePool.pool), u !== n && (a.flags |= 2048)), l !== e && l && (t.child.flags |= 8192), bu(t, t.updateQueue), _e(t), null);
        case 4:
            return qe(), e === null && es(t.stateNode.containerInfo), _e(t), null;
        case 10:
            return wt(t.type), _e(t), null;
        case 19:
            if (A(Be), a = t.memoizedState, a === null) return _e(t), null;
            if (n = (t.flags & 128) !== 0, u = a.rendering, u === null)
                if (n) fn(a, !1);
                else {
                    if (He !== 0 || e !== null && (e.flags & 128) !== 0)
                        for (e = t.child; e !== null;) {
                            if (u = cu(e), u !== null) {
                                for (t.flags |= 128, fn(a, !1), e = u.updateQueue, t.updateQueue = e, bu(t, e), t.subtreeFlags = 0, e = l, l = t.child; l !== null;) Cf(l, e), l = l.sibling;
                                return B(Be, Be.current & 1 | 2), re && Qt(t, a.treeForkCount), t.child
                            }
                            e = e.sibling
                        }
                    a.tail !== null && rt() > zu && (t.flags |= 128, n = !0, fn(a, !1), t.lanes = 4194304)
                }
            else {
                if (!n)
                    if (e = cu(u), e !== null) {
                        if (t.flags |= 128, n = !0, e = e.updateQueue, t.updateQueue = e, bu(t, e), fn(a, !0), a.tail === null && a.tailMode === "hidden" && !u.alternate && !re) return _e(t), null
                    } else 2 * rt() - a.renderingStartTime > zu && l !== 536870912 && (t.flags |= 128, n = !0, fn(a, !1), t.lanes = 4194304);
                a.isBackwards ? (u.sibling = t.child, t.child = u) : (e = a.last, e !== null ? e.sibling = u : t.child = u, a.last = u)
            }
            return a.tail !== null ? (e = a.tail, a.rendering = e, a.tail = e.sibling, a.renderingStartTime = rt(), e.sibling = null, l = Be.current, B(Be, n ? l & 1 | 2 : l & 1), re && Qt(t, a.treeForkCount), e) : (_e(t), null);
        case 22:
        case 23:
            return yt(t), tc(), a = t.memoizedState !== null, e !== null ? e.memoizedState !== null !== a && (t.flags |= 8192) : a && (t.flags |= 8192), a ? (l & 536870912) !== 0 && (t.flags & 128) === 0 && (_e(t), t.subtreeFlags & 6 && (t.flags |= 8192)) : _e(t), l = t.updateQueue, l !== null && bu(t, l.retryQueue), l = null, e !== null && e.memoizedState !== null && e.memoizedState.cachePool !== null && (l = e.memoizedState.cachePool.pool), a = null, t.memoizedState !== null && t.memoizedState.cachePool !== null && (a = t.memoizedState.cachePool.pool), a !== l && (t.flags |= 2048), e !== null && A(kl), null;
        case 24:
            return l = null, e !== null && (l = e.memoizedState.cache), t.memoizedState.cache !== l && (t.flags |= 2048), wt(ke), _e(t), null;
        case 25:
            return null;
        case 30:
            return null
        }
        throw Error(o(156, t.tag))
    }

    function Ah(e, t) {
        switch (Yi(t), t.tag) {
        case 1:
            return e = t.flags, e & 65536 ? (t.flags = e & -65537 | 128, t) : null;
        case 3:
            return wt(ke), qe(), e = t.flags, (e & 65536) !== 0 && (e & 128) === 0 ? (t.flags = e & -65537 | 128, t) : null;
        case 26:
        case 27:
        case 5:
            return On(t), null;
        case 31:
            if (t.memoizedState !== null) {
                if (yt(t), t.alternate === null) throw Error(o(340));
                ql()
            }
            return e = t.flags, e & 65536 ? (t.flags = e & -65537 | 128, t) : null;
        case 13:
            if (yt(t), e = t.memoizedState, e !== null && e.dehydrated !== null) {
                if (t.alternate === null) throw Error(o(340));
                ql()
            }
            return e = t.flags, e & 65536 ? (t.flags = e & -65537 | 128, t) : null;
        case 19:
            return A(Be), null;
        case 4:
            return qe(), null;
        case 10:
            return wt(t.type), null;
        case 22:
        case 23:
            return yt(t), tc(), e !== null && A(kl), e = t.flags, e & 65536 ? (t.flags = e & -65537 | 128, t) : null;
        case 24:
            return wt(ke), null;
        case 25:
            return null;
        default:
            return null
        }
    }

    function sr(e, t) {
        switch (Yi(t), t.tag) {
        case 3:
            wt(ke), qe();
            break;
        case 26:
        case 27:
        case 5:
            On(t);
            break;
        case 4:
            qe();
            break;
        case 31:
            t.memoizedState !== null && yt(t);
            break;
        case 13:
            yt(t);
            break;
        case 19:
            A(Be);
            break;
        case 10:
            wt(t.type);
            break;
        case 22:
        case 23:
            yt(t), tc(), e !== null && A(kl);
            break;
        case 24:
            wt(ke)
        }
    }

    function on(e, t) {
        try {
            var l = t.updateQueue,
                a = l !== null ? l.lastEffect : null;
            if (a !== null) {
                var n = a.next;
                l = n;
                do {
                    if ((l.tag & e) === e) {
                        a = void 0;
                        var u = l.create,
                            i = l.inst;
                        a = u(), i.destroy = a
                    }
                    l = l.next
                } while (l !== n)
            }
        } catch (s) {
            ye(t, t.return, s)
        }
    }

    function vl(e, t, l) {
        try {
            var a = t.updateQueue,
                n = a !== null ? a.lastEffect : null;
            if (n !== null) {
                var u = n.next;
                a = u;
                do {
                    if ((a.tag & e) === e) {
                        var i = a.inst,
                            s = i.destroy;
                        if (s !== void 0) {
                            i.destroy = void 0, n = t;
                            var r = l,
                                y = s;
                            try {
                                y()
                            } catch (T) {
                                ye(n, r, T)
                            }
                        }
                    }
                    a = a.next
                } while (a !== u)
            }
        } catch (T) {
            ye(t, t.return, T)
        }
    }

    function fr(e) {
        var t = e.updateQueue;
        if (t !== null) {
            var l = e.stateNode;
            try {
                If(t, l)
            } catch (a) {
                ye(e, e.return, a)
            }
        }
    }

    function or(e, t, l) {
        l.props = Vl(e.type, e.memoizedProps), l.state = e.memoizedState;
        try {
            l.componentWillUnmount()
        } catch (a) {
            ye(e, t, a)
        }
    }

    function rn(e, t) {
        try {
            var l = e.ref;
            if (l !== null) {
                switch (e.tag) {
                case 26:
                case 27:
                case 5:
                    var a = e.stateNode;
                    break;
                case 30:
                    a = e.stateNode;
                    break;
                default:
                    a = e.stateNode
                }
                typeof l == "function" ? e.refCleanup = l(a) : l.current = a
            }
        } catch (n) {
            ye(e, t, n)
        }
    }

    function Bt(e, t) {
        var l = e.ref,
            a = e.refCleanup;
        if (l !== null)
            if (typeof a == "function") try {
                a()
            } catch (n) {
                ye(e, t, n)
            } finally {
                e.refCleanup = null, e = e.alternate, e != null && (e.refCleanup = null)
            } else if (typeof l == "function") try {
                l(null)
            } catch (n) {
                ye(e, t, n)
            } else l.current = null
    }

    function rr(e) {
        var t = e.type,
            l = e.memoizedProps,
            a = e.stateNode;
        try {
            e: switch (t) {
            case "button":
            case "input":
            case "select":
            case "textarea":
                l.autoFocus && a.focus();
                break e;
            case "img":
                l.src ? a.src = l.src : l.srcSet && (a.srcset = l.srcSet)
            }
        }
        catch (n) {
            ye(e, e.return, n)
        }
    }

    function Uc(e, t, l) {
        try {
            var a = e.stateNode;
            Fh(a, e.type, l, t), a[at] = t
        } catch (n) {
            ye(e, e.return, n)
        }
    }

    function dr(e) {
        return e.tag === 5 || e.tag === 3 || e.tag === 26 || e.tag === 27 && El(e.type) || e.tag === 4
    }

    function Cc(e) {
        e: for (;;) {
            for (; e.sibling === null;) {
                if (e.return === null || dr(e.return)) return null;
                e = e.return
            }
            for (e.sibling.return = e.return, e = e.sibling; e.tag !== 5 && e.tag !== 6 && e.tag !== 18;) {
                if (e.tag === 27 && El(e.type) || e.flags & 2 || e.child === null || e.tag === 4) continue e;
                e.child.return = e, e = e.child
            }
            if (!(e.flags & 2)) return e.stateNode
        }
    }

    function Hc(e, t, l) {
        var a = e.tag;
        if (a === 5 || a === 6) e = e.stateNode, t ? (l.nodeType === 9 ? l.body : l.nodeName === "HTML" ? l.ownerDocument.body : l).insertBefore(e, t) : (t = l.nodeType === 9 ? l.body : l.nodeName === "HTML" ? l.ownerDocument.body : l, t.appendChild(e), l = l._reactRootContainer, l != null || t.onclick !== null || (t.onclick = Yt));
        else if (a !== 4 && (a === 27 && El(e.type) && (l = e.stateNode, t = null), e = e.child, e !== null))
            for (Hc(e, t, l), e = e.sibling; e !== null;) Hc(e, t, l), e = e.sibling
    }

    function Nu(e, t, l) {
        var a = e.tag;
        if (a === 5 || a === 6) e = e.stateNode, t ? l.insertBefore(e, t) : l.appendChild(e);
        else if (a !== 4 && (a === 27 && El(e.type) && (l = e.stateNode), e = e.child, e !== null))
            for (Nu(e, t, l), e = e.sibling; e !== null;) Nu(e, t, l), e = e.sibling
    }

    function mr(e) {
        var t = e.stateNode,
            l = e.memoizedProps;
        try {
            for (var a = e.type, n = t.attributes; n.length;) t.removeAttributeNode(n[0]);
            Fe(t, a, l), t[Ke] = e, t[at] = l
        } catch (u) {
            ye(e, e.return, u)
        }
    }
    var $t = !1,
        Xe = !1,
        qc = !1,
        hr = typeof WeakSet == "function" ? WeakSet : Set,
        we = null;

    function _h(e, t) {
        if (e = e.containerInfo, as = Xu, e = zf(e), Ai(e)) {
            if ("selectionStart" in e) var l = {
                start: e.selectionStart,
                end: e.selectionEnd
            };
            else e: {
                l = (l = e.ownerDocument) && l.defaultView || window;
                var a = l.getSelection && l.getSelection();
                if (a && a.rangeCount !== 0) {
                    l = a.anchorNode;
                    var n = a.anchorOffset,
                        u = a.focusNode;
                    a = a.focusOffset;
                    try {
                        l.nodeType, u.nodeType
                    } catch {
                        l = null;
                        break e
                    }
                    var i = 0,
                        s = -1,
                        r = -1,
                        y = 0,
                        T = 0,
                        D = e,
                        p = null;
                    t: for (;;) {
                        for (var E; D !== l || n !== 0 && D.nodeType !== 3 || (s = i + n), D !== u || a !== 0 && D.nodeType !== 3 || (r = i + a), D.nodeType === 3 && (i += D.nodeValue.length), (E = D.firstChild) !== null;) p = D, D = E;
                        for (;;) {
                            if (D === e) break t;
                            if (p === l && ++y === n && (s = i), p === u && ++T === a && (r = i), (E = D.nextSibling) !== null) break;
                            D = p, p = D.parentNode
                        }
                        D = E
                    }
                    l = s === -1 || r === -1 ? null : {
                        start: s,
                        end: r
                    }
                } else l = null
            }
            l = l || {
                start: 0,
                end: 0
            }
        } else l = null;
        for (ns = {
                focusedElem: e,
                selectionRange: l
            }, Xu = !1, we = t; we !== null;)
            if (t = we, e = t.child, (t.subtreeFlags & 1028) !== 0 && e !== null) e.return = t, we = e;
            else
                for (; we !== null;) {
                    switch (t = we, u = t.alternate, e = t.flags, t.tag) {
                    case 0:
                        if ((e & 4) !== 0 && (e = t.updateQueue, e = e !== null ? e.events : null, e !== null))
                            for (l = 0; l < e.length; l++) n = e[l], n.ref.impl = n.nextImpl;
                        break;
                    case 11:
                    case 15:
                        break;
                    case 1:
                        if ((e & 1024) !== 0 && u !== null) {
                            e = void 0, l = t, n = u.memoizedProps, u = u.memoizedState, a = l.stateNode;
                            try {
                                var k = Vl(l.type, n);
                                e = a.getSnapshotBeforeUpdate(k, u), a.__reactInternalSnapshotBeforeUpdate = e
                            } catch ($) {
                                ye(l, l.return, $)
                            }
                        }
                        break;
                    case 3:
                        if ((e & 1024) !== 0) {
                            if (e = t.stateNode.containerInfo, l = e.nodeType, l === 9) cs(e);
                            else if (l === 1) switch (e.nodeName) {
                            case "HEAD":
                            case "HTML":
                            case "BODY":
                                cs(e);
                                break;
                            default:
                                e.textContent = ""
                            }
                        }
                        break;
                    case 5:
                    case 26:
                    case 27:
                    case 6:
                    case 4:
                    case 17:
                        break;
                    default:
                        if ((e & 1024) !== 0) throw Error(o(163))
                    }
                    if (e = t.sibling, e !== null) {
                        e.return = t.return, we = e;
                        break
                    }
                    we = t.return
                }
    }

    function vr(e, t, l) {
        var a = l.flags;
        switch (l.tag) {
        case 0:
        case 11:
        case 15:
            It(e, l), a & 4 && on(5, l);
            break;
        case 1:
            if (It(e, l), a & 4)
                if (e = l.stateNode, t === null) try {
                    e.componentDidMount()
                } catch (i) {
                    ye(l, l.return, i)
                } else {
                    var n = Vl(l.type, t.memoizedProps);
                    t = t.memoizedState;
                    try {
                        e.componentDidUpdate(n, t, e.__reactInternalSnapshotBeforeUpdate)
                    } catch (i) {
                        ye(l, l.return, i)
                    }
                }
            a & 64 && fr(l), a & 512 && rn(l, l.return);
            break;
        case 3:
            if (It(e, l), a & 64 && (e = l.updateQueue, e !== null)) {
                if (t = null, l.child !== null) switch (l.child.tag) {
                case 27:
                case 5:
                    t = l.child.stateNode;
                    break;
                case 1:
                    t = l.child.stateNode
                }
                try {
                    If(e, t)
                } catch (i) {
                    ye(l, l.return, i)
                }
            }
            break;
        case 27:
            t === null && a & 4 && mr(l);
        case 26:
        case 5:
            It(e, l), t === null && a & 4 && rr(l), a & 512 && rn(l, l.return);
            break;
        case 12:
            It(e, l);
            break;
        case 31:
            It(e, l), a & 4 && pr(e, l);
            break;
        case 13:
            It(e, l), a & 4 && Sr(e, l), a & 64 && (e = l.memoizedState, e !== null && (e = e.dehydrated, e !== null && (l = kh.bind(null, l), u1(e, l))));
            break;
        case 22:
            if (a = l.memoizedState !== null || $t, !a) {
                t = t !== null && t.memoizedState !== null || Xe, n = $t;
                var u = Xe;
                $t = a, (Xe = t) && !u ? Pt(e, l, (l.subtreeFlags & 8772) !== 0) : It(e, l), $t = n, Xe = u
            }
            break;
        case 30:
            break;
        default:
            It(e, l)
        }
    }

    function gr(e) {
        var t = e.alternate;
        t !== null && (e.alternate = null, gr(t)), e.child = null, e.deletions = null, e.sibling = null, e.tag === 5 && (t = e.stateNode, t !== null && di(t)), e.stateNode = null, e.return = null, e.dependencies = null, e.memoizedProps = null, e.memoizedState = null, e.pendingProps = null, e.stateNode = null, e.updateQueue = null
    }
    var Oe = null,
        ut = !1;

    function Ft(e, t, l) {
        for (l = l.child; l !== null;) yr(e, t, l), l = l.sibling
    }

    function yr(e, t, l) {
        if (dt && typeof dt.onCommitFiberUnmount == "function") try {
            dt.onCommitFiberUnmount(Ca, l)
        } catch {}
        switch (l.tag) {
        case 26:
            Xe || Bt(l, t), Ft(e, t, l), l.memoizedState ? l.memoizedState.count-- : l.stateNode && (l = l.stateNode, l.parentNode.removeChild(l));
            break;
        case 27:
            Xe || Bt(l, t);
            var a = Oe,
                n = ut;
            El(l.type) && (Oe = l.stateNode, ut = !1), Ft(e, t, l), bn(l.stateNode), Oe = a, ut = n;
            break;
        case 5:
            Xe || Bt(l, t);
        case 6:
            if (a = Oe, n = ut, Oe = null, Ft(e, t, l), Oe = a, ut = n, Oe !== null)
                if (ut) try {
                    (Oe.nodeType === 9 ? Oe.body : Oe.nodeName === "HTML" ? Oe.ownerDocument.body : Oe).removeChild(l.stateNode)
                } catch (u) {
                    ye(l, t, u)
                } else try {
                    Oe.removeChild(l.stateNode)
                } catch (u) {
                    ye(l, t, u)
                }
            break;
        case 18:
            Oe !== null && (ut ? (e = Oe, fd(e.nodeType === 9 ? e.body : e.nodeName === "HTML" ? e.ownerDocument.body : e, l.stateNode), _a(e)) : fd(Oe, l.stateNode));
            break;
        case 4:
            a = Oe, n = ut, Oe = l.stateNode.containerInfo, ut = !0, Ft(e, t, l), Oe = a, ut = n;
            break;
        case 0:
        case 11:
        case 14:
        case 15:
            vl(2, l, t), Xe || vl(4, l, t), Ft(e, t, l);
            break;
        case 1:
            Xe || (Bt(l, t), a = l.stateNode, typeof a.componentWillUnmount == "function" && or(l, t, a)), Ft(e, t, l);
            break;
        case 21:
            Ft(e, t, l);
            break;
        case 22:
            Xe = (a = Xe) || l.memoizedState !== null, Ft(e, t, l), Xe = a;
            break;
        default:
            Ft(e, t, l)
        }
    }

    function pr(e, t) {
        if (t.memoizedState === null && (e = t.alternate, e !== null && (e = e.memoizedState, e !== null))) {
            e = e.dehydrated;
            try {
                _a(e)
            } catch (l) {
                ye(t, t.return, l)
            }
        }
    }

    function Sr(e, t) {
        if (t.memoizedState === null && (e = t.alternate, e !== null && (e = e.memoizedState, e !== null && (e = e.dehydrated, e !== null)))) try {
            _a(e)
        } catch (l) {
            ye(t, t.return, l)
        }
    }

    function Oh(e) {
        switch (e.tag) {
        case 31:
        case 13:
        case 19:
            var t = e.stateNode;
            return t === null && (t = e.stateNode = new hr), t;
        case 22:
            return e = e.stateNode, t = e._retryCache, t === null && (t = e._retryCache = new hr), t;
        default:
            throw Error(o(435, e.tag))
        }
    }

    function Eu(e, t) {
        var l = Oh(e);
        t.forEach(function (a) {
            if (!l.has(a)) {
                l.add(a);
                var n = Yh.bind(null, e, a);
                a.then(n, n)
            }
        })
    }

    function it(e, t) {
        var l = t.deletions;
        if (l !== null)
            for (var a = 0; a < l.length; a++) {
                var n = l[a],
                    u = e,
                    i = t,
                    s = i;
                e: for (; s !== null;) {
                    switch (s.tag) {
                    case 27:
                        if (El(s.type)) {
                            Oe = s.stateNode, ut = !1;
                            break e
                        }
                        break;
                    case 5:
                        Oe = s.stateNode, ut = !1;
                        break e;
                    case 3:
                    case 4:
                        Oe = s.stateNode.containerInfo, ut = !0;
                        break e
                    }
                    s = s.return
                }
                if (Oe === null) throw Error(o(160));
                yr(u, i, n), Oe = null, ut = !1, u = n.alternate, u !== null && (u.return = null), n.return = null
            }
        if (t.subtreeFlags & 13886)
            for (t = t.child; t !== null;) br(t, e), t = t.sibling
    }
    var Rt = null;

    function br(e, t) {
        var l = e.alternate,
            a = e.flags;
        switch (e.tag) {
        case 0:
        case 11:
        case 14:
        case 15:
            it(t, e), ct(e), a & 4 && (vl(3, e, e.return), on(3, e), vl(5, e, e.return));
            break;
        case 1:
            it(t, e), ct(e), a & 512 && (Xe || l === null || Bt(l, l.return)), a & 64 && $t && (e = e.updateQueue, e !== null && (a = e.callbacks, a !== null && (l = e.shared.hiddenCallbacks, e.shared.hiddenCallbacks = l === null ? a : l.concat(a))));
            break;
        case 26:
            var n = Rt;
            if (it(t, e), ct(e), a & 512 && (Xe || l === null || Bt(l, l.return)), a & 4) {
                var u = l !== null ? l.memoizedState : null;
                if (a = e.memoizedState, l === null)
                    if (a === null)
                        if (e.stateNode === null) {
                            e: {
                                a = e.type,
                                l = e.memoizedProps,
                                n = n.ownerDocument || n;t: switch (a) {
                                case "title":
                                    u = n.getElementsByTagName("title")[0], (!u || u[Ba] || u[Ke] || u.namespaceURI === "http://www.w3.org/2000/svg" || u.hasAttribute("itemprop")) && (u = n.createElement(a), n.head.insertBefore(u, n.querySelector("head > title"))), Fe(u, a, l), u[Ke] = e, Ve(u), a = u;
                                    break e;
                                case "link":
                                    var i = bd("link", "href", n).get(a + (l.href || ""));
                                    if (i) {
                                        for (var s = 0; s < i.length; s++)
                                            if (u = i[s], u.getAttribute("href") === (l.href == null || l.href === "" ? null : l.href) && u.getAttribute("rel") === (l.rel == null ? null : l.rel) && u.getAttribute("title") === (l.title == null ? null : l.title) && u.getAttribute("crossorigin") === (l.crossOrigin == null ? null : l.crossOrigin)) {
                                                i.splice(s, 1);
                                                break t
                                            }
                                    }
                                    u = n.createElement(a), Fe(u, a, l), n.head.appendChild(u);
                                    break;
                                case "meta":
                                    if (i = bd("meta", "content", n).get(a + (l.content || ""))) {
                                        for (s = 0; s < i.length; s++)
                                            if (u = i[s], u.getAttribute("content") === (l.content == null ? null : "" + l.content) && u.getAttribute("name") === (l.name == null ? null : l.name) && u.getAttribute("property") === (l.property == null ? null : l.property) && u.getAttribute("http-equiv") === (l.httpEquiv == null ? null : l.httpEquiv) && u.getAttribute("charset") === (l.charSet == null ? null : l.charSet)) {
                                                i.splice(s, 1);
                                                break t
                                            }
                                    }
                                    u = n.createElement(a), Fe(u, a, l), n.head.appendChild(u);
                                    break;
                                default:
                                    throw Error(o(468, a))
                                }
                                u[Ke] = e,
                                Ve(u),
                                a = u
                            }
                            e.stateNode = a
                        }
                else Nd(n, e.type, e.stateNode);
                else e.stateNode = Sd(n, a, e.memoizedProps);
                else u !== a ? (u === null ? l.stateNode !== null && (l = l.stateNode, l.parentNode.removeChild(l)) : u.count--, a === null ? Nd(n, e.type, e.stateNode) : Sd(n, a, e.memoizedProps)) : a === null && e.stateNode !== null && Uc(e, e.memoizedProps, l.memoizedProps)
            }
            break;
        case 27:
            it(t, e), ct(e), a & 512 && (Xe || l === null || Bt(l, l.return)), l !== null && a & 4 && Uc(e, e.memoizedProps, l.memoizedProps);
            break;
        case 5:
            if (it(t, e), ct(e), a & 512 && (Xe || l === null || Bt(l, l.return)), e.flags & 32) {
                n = e.stateNode;
                try {
                    Pl(n, "")
                } catch (k) {
                    ye(e, e.return, k)
                }
            }
            a & 4 && e.stateNode != null && (n = e.memoizedProps, Uc(e, n, l !== null ? l.memoizedProps : n)), a & 1024 && (qc = !0);
            break;
        case 6:
            if (it(t, e), ct(e), a & 4) {
                if (e.stateNode === null) throw Error(o(162));
                a = e.memoizedProps, l = e.stateNode;
                try {
                    l.nodeValue = a
                } catch (k) {
                    ye(e, e.return, k)
                }
            }
            break;
        case 3:
            if (Lu = null, n = Rt, Rt = qu(t.containerInfo), it(t, e), Rt = n, ct(e), a & 4 && l !== null && l.memoizedState.isDehydrated) try {
                _a(t.containerInfo)
            } catch (k) {
                ye(e, e.return, k)
            }
            qc && (qc = !1, Nr(e));
            break;
        case 4:
            a = Rt, Rt = qu(e.stateNode.containerInfo), it(t, e), ct(e), Rt = a;
            break;
        case 12:
            it(t, e), ct(e);
            break;
        case 31:
            it(t, e), ct(e), a & 4 && (a = e.updateQueue, a !== null && (e.updateQueue = null, Eu(e, a)));
            break;
        case 13:
            it(t, e), ct(e), e.child.flags & 8192 && e.memoizedState !== null != (l !== null && l.memoizedState !== null) && (xu = rt()), a & 4 && (a = e.updateQueue, a !== null && (e.updateQueue = null, Eu(e, a)));
            break;
        case 22:
            n = e.memoizedState !== null;
            var r = l !== null && l.memoizedState !== null,
                y = $t,
                T = Xe;
            if ($t = y || n, Xe = T || r, it(t, e), Xe = T, $t = y, ct(e), a & 8192) e: for (t = e.stateNode, t._visibility = n ? t._visibility & -2 : t._visibility | 1, n && (l === null || r || $t || Xe || wl(e)), l = null, t = e;;) {
                if (t.tag === 5 || t.tag === 26) {
                    if (l === null) {
                        r = l = t;
                        try {
                            if (u = r.stateNode, n) i = u.style, typeof i.setProperty == "function" ? i.setProperty("display", "none", "important") : i.display = "none";
                            else {
                                s = r.stateNode;
                                var D = r.memoizedProps.style,
                                    p = D != null && D.hasOwnProperty("display") ? D.display : null;
                                s.style.display = p == null || typeof p == "boolean" ? "" : ("" + p).trim()
                            }
                        } catch (k) {
                            ye(r, r.return, k)
                        }
                    }
                } else if (t.tag === 6) {
                    if (l === null) {
                        r = t;
                        try {
                            r.stateNode.nodeValue = n ? "" : r.memoizedProps
                        } catch (k) {
                            ye(r, r.return, k)
                        }
                    }
                } else if (t.tag === 18) {
                    if (l === null) {
                        r = t;
                        try {
                            var E = r.stateNode;
                            n ? od(E, !0) : od(r.stateNode, !1)
                        } catch (k) {
                            ye(r, r.return, k)
                        }
                    }
                } else if ((t.tag !== 22 && t.tag !== 23 || t.memoizedState === null || t === e) && t.child !== null) {
                    t.child.return = t, t = t.child;
                    continue
                }
                if (t === e) break e;
                for (; t.sibling === null;) {
                    if (t.return === null || t.return === e) break e;
                    l === t && (l = null), t = t.return
                }
                l === t && (l = null), t.sibling.return = t.return, t = t.sibling
            }
            a & 4 && (a = e.updateQueue, a !== null && (l = a.retryQueue, l !== null && (a.retryQueue = null, Eu(e, l))));
            break;
        case 19:
            it(t, e), ct(e), a & 4 && (a = e.updateQueue, a !== null && (e.updateQueue = null, Eu(e, a)));
            break;
        case 30:
            break;
        case 21:
            break;
        default:
            it(t, e), ct(e)
        }
    }

    function ct(e) {
        var t = e.flags;
        if (t & 2) {
            try {
                for (var l, a = e.return; a !== null;) {
                    if (dr(a)) {
                        l = a;
                        break
                    }
                    a = a.return
                }
                if (l == null) throw Error(o(160));
                switch (l.tag) {
                case 27:
                    var n = l.stateNode,
                        u = Cc(e);
                    Nu(e, u, n);
                    break;
                case 5:
                    var i = l.stateNode;
                    l.flags & 32 && (Pl(i, ""), l.flags &= -33);
                    var s = Cc(e);
                    Nu(e, s, i);
                    break;
                case 3:
                case 4:
                    var r = l.stateNode.containerInfo,
                        y = Cc(e);
                    Hc(e, y, r);
                    break;
                default:
                    throw Error(o(161))
                }
            } catch (T) {
                ye(e, e.return, T)
            }
            e.flags &= -3
        }
        t & 4096 && (e.flags &= -4097)
    }

    function Nr(e) {
        if (e.subtreeFlags & 1024)
            for (e = e.child; e !== null;) {
                var t = e;
                Nr(t), t.tag === 5 && t.flags & 1024 && t.stateNode.reset(), e = e.sibling
            }
    }

    function It(e, t) {
        if (t.subtreeFlags & 8772)
            for (t = t.child; t !== null;) vr(e, t.alternate, t), t = t.sibling
    }

    function wl(e) {
        for (e = e.child; e !== null;) {
            var t = e;
            switch (t.tag) {
            case 0:
            case 11:
            case 14:
            case 15:
                vl(4, t, t.return), wl(t);
                break;
            case 1:
                Bt(t, t.return);
                var l = t.stateNode;
                typeof l.componentWillUnmount == "function" && or(t, t.return, l), wl(t);
                break;
            case 27:
                bn(t.stateNode);
            case 26:
            case 5:
                Bt(t, t.return), wl(t);
                break;
            case 22:
                t.memoizedState === null && wl(t);
                break;
            case 30:
                wl(t);
                break;
            default:
                wl(t)
            }
            e = e.sibling
        }
    }

    function Pt(e, t, l) {
        for (l = l && (t.subtreeFlags & 8772) !== 0, t = t.child; t !== null;) {
            var a = t.alternate,
                n = e,
                u = t,
                i = u.flags;
            switch (u.tag) {
            case 0:
            case 11:
            case 15:
                Pt(n, u, l), on(4, u);
                break;
            case 1:
                if (Pt(n, u, l), a = u, n = a.stateNode, typeof n.componentDidMount == "function") try {
                    n.componentDidMount()
                } catch (y) {
                    ye(a, a.return, y)
                }
                if (a = u, n = a.updateQueue, n !== null) {
                    var s = a.stateNode;
                    try {
                        var r = n.shared.hiddenCallbacks;
                        if (r !== null)
                            for (n.shared.hiddenCallbacks = null, n = 0; n < r.length; n++) Ff(r[n], s)
                    } catch (y) {
                        ye(a, a.return, y)
                    }
                }
                l && i & 64 && fr(u), rn(u, u.return);
                break;
            case 27:
                mr(u);
            case 26:
            case 5:
                Pt(n, u, l), l && a === null && i & 4 && rr(u), rn(u, u.return);
                break;
            case 12:
                Pt(n, u, l);
                break;
            case 31:
                Pt(n, u, l), l && i & 4 && pr(n, u);
                break;
            case 13:
                Pt(n, u, l), l && i & 4 && Sr(n, u);
                break;
            case 22:
                u.memoizedState === null && Pt(n, u, l), rn(u, u.return);
                break;
            case 30:
                break;
            default:
                Pt(n, u, l)
            }
            t = t.sibling
        }
    }

    function Bc(e, t) {
        var l = null;
        e !== null && e.memoizedState !== null && e.memoizedState.cachePool !== null && (l = e.memoizedState.cachePool.pool), e = null, t.memoizedState !== null && t.memoizedState.cachePool !== null && (e = t.memoizedState.cachePool.pool), e !== l && (e != null && e.refCount++, l != null && $a(l))
    }

    function Lc(e, t) {
        e = null, t.alternate !== null && (e = t.alternate.memoizedState.cache), t = t.memoizedState.cache, t !== e && (t.refCount++, e != null && $a(e))
    }

    function Ut(e, t, l, a) {
        if (t.subtreeFlags & 10256)
            for (t = t.child; t !== null;) Er(e, t, l, a), t = t.sibling
    }

    function Er(e, t, l, a) {
        var n = t.flags;
        switch (t.tag) {
        case 0:
        case 11:
        case 15:
            Ut(e, t, l, a), n & 2048 && on(9, t);
            break;
        case 1:
            Ut(e, t, l, a);
            break;
        case 3:
            Ut(e, t, l, a), n & 2048 && (e = null, t.alternate !== null && (e = t.alternate.memoizedState.cache), t = t.memoizedState.cache, t !== e && (t.refCount++, e != null && $a(e)));
            break;
        case 12:
            if (n & 2048) {
                Ut(e, t, l, a), e = t.stateNode;
                try {
                    var u = t.memoizedProps,
                        i = u.id,
                        s = u.onPostCommit;
                    typeof s == "function" && s(i, t.alternate === null ? "mount" : "update", e.passiveEffectDuration, -0)
                } catch (r) {
                    ye(t, t.return, r)
                }
            } else Ut(e, t, l, a);
            break;
        case 31:
            Ut(e, t, l, a);
            break;
        case 13:
            Ut(e, t, l, a);
            break;
        case 23:
            break;
        case 22:
            u = t.stateNode, i = t.alternate, t.memoizedState !== null ? u._visibility & 2 ? Ut(e, t, l, a) : dn(e, t) : u._visibility & 2 ? Ut(e, t, l, a) : (u._visibility |= 2, Sa(e, t, l, a, (t.subtreeFlags & 10256) !== 0 || !1)), n & 2048 && Bc(i, t);
            break;
        case 24:
            Ut(e, t, l, a), n & 2048 && Lc(t.alternate, t);
            break;
        default:
            Ut(e, t, l, a)
        }
    }

    function Sa(e, t, l, a, n) {
        for (n = n && ((t.subtreeFlags & 10256) !== 0 || !1), t = t.child; t !== null;) {
            var u = e,
                i = t,
                s = l,
                r = a,
                y = i.flags;
            switch (i.tag) {
            case 0:
            case 11:
            case 15:
                Sa(u, i, s, r, n), on(8, i);
                break;
            case 23:
                break;
            case 22:
                var T = i.stateNode;
                i.memoizedState !== null ? T._visibility & 2 ? Sa(u, i, s, r, n) : dn(u, i) : (T._visibility |= 2, Sa(u, i, s, r, n)), n && y & 2048 && Bc(i.alternate, i);
                break;
            case 24:
                Sa(u, i, s, r, n), n && y & 2048 && Lc(i.alternate, i);
                break;
            default:
                Sa(u, i, s, r, n)
            }
            t = t.sibling
        }
    }

    function dn(e, t) {
        if (t.subtreeFlags & 10256)
            for (t = t.child; t !== null;) {
                var l = e,
                    a = t,
                    n = a.flags;
                switch (a.tag) {
                case 22:
                    dn(l, a), n & 2048 && Bc(a.alternate, a);
                    break;
                case 24:
                    dn(l, a), n & 2048 && Lc(a.alternate, a);
                    break;
                default:
                    dn(l, a)
                }
                t = t.sibling
            }
    }
    var mn = 8192;

    function ba(e, t, l) {
        if (e.subtreeFlags & mn)
            for (e = e.child; e !== null;) Tr(e, t, l), e = e.sibling
    }

    function Tr(e, t, l) {
        switch (e.tag) {
        case 26:
            ba(e, t, l), e.flags & mn && e.memoizedState !== null && y1(l, Rt, e.memoizedState, e.memoizedProps);
            break;
        case 5:
            ba(e, t, l);
            break;
        case 3:
        case 4:
            var a = Rt;
            Rt = qu(e.stateNode.containerInfo), ba(e, t, l), Rt = a;
            break;
        case 22:
            e.memoizedState === null && (a = e.alternate, a !== null && a.memoizedState !== null ? (a = mn, mn = 16777216, ba(e, t, l), mn = a) : ba(e, t, l));
            break;
        default:
            ba(e, t, l)
        }
    }

    function xr(e) {
        var t = e.alternate;
        if (t !== null && (e = t.child, e !== null)) {
            t.child = null;
            do t = e.sibling, e.sibling = null, e = t; while (e !== null)
        }
    }

    function hn(e) {
        var t = e.deletions;
        if ((e.flags & 16) !== 0) {
            if (t !== null)
                for (var l = 0; l < t.length; l++) {
                    var a = t[l];
                    we = a, jr(a, e)
                }
            xr(e)
        }
        if (e.subtreeFlags & 10256)
            for (e = e.child; e !== null;) zr(e), e = e.sibling
    }

    function zr(e) {
        switch (e.tag) {
        case 0:
        case 11:
        case 15:
            hn(e), e.flags & 2048 && vl(9, e, e.return);
            break;
        case 3:
            hn(e);
            break;
        case 12:
            hn(e);
            break;
        case 22:
            var t = e.stateNode;
            e.memoizedState !== null && t._visibility & 2 && (e.return === null || e.return.tag !== 13) ? (t._visibility &= -3, Tu(e)) : hn(e);
            break;
        default:
            hn(e)
        }
    }

    function Tu(e) {
        var t = e.deletions;
        if ((e.flags & 16) !== 0) {
            if (t !== null)
                for (var l = 0; l < t.length; l++) {
                    var a = t[l];
                    we = a, jr(a, e)
                }
            xr(e)
        }
        for (e = e.child; e !== null;) {
            switch (t = e, t.tag) {
            case 0:
            case 11:
            case 15:
                vl(8, t, t.return), Tu(t);
                break;
            case 22:
                l = t.stateNode, l._visibility & 2 && (l._visibility &= -3, Tu(t));
                break;
            default:
                Tu(t)
            }
            e = e.sibling
        }
    }

    function jr(e, t) {
        for (; we !== null;) {
            var l = we;
            switch (l.tag) {
            case 0:
            case 11:
            case 15:
                vl(8, l, t);
                break;
            case 23:
            case 22:
                if (l.memoizedState !== null && l.memoizedState.cachePool !== null) {
                    var a = l.memoizedState.cachePool.pool;
                    a != null && a.refCount++
                }
                break;
            case 24:
                $a(l.memoizedState.cache)
            }
            if (a = l.child, a !== null) a.return = l, we = a;
            else e: for (l = e; we !== null;) {
                a = we;
                var n = a.sibling,
                    u = a.return;
                if (gr(a), a === l) {
                    we = null;
                    break e
                }
                if (n !== null) {
                    n.return = u, we = n;
                    break e
                }
                we = u
            }
        }
    }
    var Rh = {
            getCacheForType: function (e) {
                var t = We(ke),
                    l = t.data.get(e);
                return l === void 0 && (l = e(), t.data.set(e, l)), l
            },
            cacheSignal: function () {
                return We(ke).controller.signal
            }
        },
        Uh = typeof WeakMap == "function" ? WeakMap : Map,
        he = 0,
        xe = null,
        ie = null,
        fe = 0,
        ge = 0,
        pt = null,
        gl = !1,
        Na = !1,
        kc = !1,
        el = 0,
        He = 0,
        yl = 0,
        Zl = 0,
        Yc = 0,
        St = 0,
        Ea = 0,
        vn = null,
        st = null,
        Gc = !1,
        xu = 0,
        Mr = 0,
        zu = 1 / 0,
        ju = null,
        pl = null,
        Qe = 0,
        Sl = null,
        Ta = null,
        tl = 0,
        Xc = 0,
        Qc = null,
        Dr = null,
        gn = 0,
        Vc = null;

    function bt() {
        return (he & 2) !== 0 && fe !== 0 ? fe & -fe : x.T !== null ? $c() : Xs()
    }

    function Ar() {
        if (St === 0)
            if ((fe & 536870912) === 0 || re) {
                var e = Cn;
                Cn <<= 1, (Cn & 3932160) === 0 && (Cn = 262144), St = e
            } else St = 536870912;
        return e = gt.current, e !== null && (e.flags |= 32), St
    }

    function ft(e, t, l) {
        (e === xe && (ge === 2 || ge === 9) || e.cancelPendingCommit !== null) && (xa(e, 0), bl(e, fe, St, !1)), qa(e, l), ((he & 2) === 0 || e !== xe) && (e === xe && ((he & 2) === 0 && (Zl |= l), He === 4 && bl(e, fe, St, !1)), Lt(e))
    }

    function _r(e, t, l) {
        if ((he & 6) !== 0) throw Error(o(327));
        var a = !l && (t & 127) === 0 && (t & e.expiredLanes) === 0 || Ha(e, t),
            n = a ? qh(e, t) : Zc(e, t, !0),
            u = a;
        do {
            if (n === 0) {
                Na && !a && bl(e, t, 0, !1);
                break
            } else {
                if (l = e.current.alternate, u && !Ch(l)) {
                    n = Zc(e, t, !1), u = !1;
                    continue
                }
                if (n === 2) {
                    if (u = t, e.errorRecoveryDisabledLanes & u) var i = 0;
                    else i = e.pendingLanes & -536870913, i = i !== 0 ? i : i & 536870912 ? 536870912 : 0;
                    if (i !== 0) {
                        t = i;
                        e: {
                            var s = e;n = vn;
                            var r = s.current.memoizedState.isDehydrated;
                            if (r && (xa(s, i).flags |= 256), i = Zc(s, i, !1), i !== 2) {
                                if (kc && !r) {
                                    s.errorRecoveryDisabledLanes |= u, Zl |= u, n = 4;
                                    break e
                                }
                                u = st, st = n, u !== null && (st === null ? st = u : st.push.apply(st, u))
                            }
                            n = i
                        }
                        if (u = !1, n !== 2) continue
                    }
                }
                if (n === 1) {
                    xa(e, 0), bl(e, t, 0, !0);
                    break
                }
                e: {
                    switch (a = e, u = n, u) {
                    case 0:
                    case 1:
                        throw Error(o(345));
                    case 4:
                        if ((t & 4194048) !== t) break;
                    case 6:
                        bl(a, t, St, !gl);
                        break e;
                    case 2:
                        st = null;
                        break;
                    case 3:
                    case 5:
                        break;
                    default:
                        throw Error(o(329))
                    }
                    if ((t & 62914560) === t && (n = xu + 300 - rt(), 10 < n)) {
                        if (bl(a, t, St, !gl), qn(a, 0, !0) !== 0) break e;
                        tl = t, a.timeoutHandle = cd(Or.bind(null, a, l, st, ju, Gc, t, St, Zl, Ea, gl, u, "Throttled", -0, 0), n);
                        break e
                    }
                    Or(a, l, st, ju, Gc, t, St, Zl, Ea, gl, u, null, -0, 0)
                }
            }
            break
        } while (!0);
        Lt(e)
    }

    function Or(e, t, l, a, n, u, i, s, r, y, T, D, p, E) {
        if (e.timeoutHandle = -1, D = t.subtreeFlags, D & 8192 || (D & 16785408) === 16785408) {
            D = {
                stylesheets: null,
                count: 0,
                imgCount: 0,
                imgBytes: 0,
                suspenseyImages: [],
                waitingForImages: !0,
                waitingForViewTransition: !1,
                unsuspend: Yt
            }, Tr(t, u, D);
            var k = (u & 62914560) === u ? xu - rt() : (u & 4194048) === u ? Mr - rt() : 0;
            if (k = p1(D, k), k !== null) {
                tl = u, e.cancelPendingCommit = k(kr.bind(null, e, t, u, l, a, n, i, s, r, T, D, null, p, E)), bl(e, u, i, !y);
                return
            }
        }
        kr(e, t, u, l, a, n, i, s, r)
    }

    function Ch(e) {
        for (var t = e;;) {
            var l = t.tag;
            if ((l === 0 || l === 11 || l === 15) && t.flags & 16384 && (l = t.updateQueue, l !== null && (l = l.stores, l !== null)))
                for (var a = 0; a < l.length; a++) {
                    var n = l[a],
                        u = n.getSnapshot;
                    n = n.value;
                    try {
                        if (!ht(u(), n)) return !1
                    } catch {
                        return !1
                    }
                }
            if (l = t.child, t.subtreeFlags & 16384 && l !== null) l.return = t, t = l;
            else {
                if (t === e) break;
                for (; t.sibling === null;) {
                    if (t.return === null || t.return === e) return !0;
                    t = t.return
                }
                t.sibling.return = t.return, t = t.sibling
            }
        }
        return !0
    }

    function bl(e, t, l, a) {
        t &= ~Yc, t &= ~Zl, e.suspendedLanes |= t, e.pingedLanes &= ~t, a && (e.warmLanes |= t), a = e.expirationTimes;
        for (var n = t; 0 < n;) {
            var u = 31 - mt(n),
                i = 1 << u;
            a[u] = -1, n &= ~i
        }
        l !== 0 && ks(e, l, t)
    }

    function Mu() {
        return (he & 6) === 0 ? (yn(0), !1) : !0
    }

    function wc() {
        if (ie !== null) {
            if (ge === 0) var e = ie.return;
            else e = ie, Vt = Bl = null, cc(e), ha = null, Ia = 0, e = ie;
            for (; e !== null;) sr(e.alternate, e), e = e.return;
            ie = null
        }
    }

    function xa(e, t) {
        var l = e.timeoutHandle;
        l !== -1 && (e.timeoutHandle = -1, e1(l)), l = e.cancelPendingCommit, l !== null && (e.cancelPendingCommit = null, l()), tl = 0, wc(), xe = e, ie = l = Xt(e.current, null), fe = t, ge = 0, pt = null, gl = !1, Na = Ha(e, t), kc = !1, Ea = St = Yc = Zl = yl = He = 0, st = vn = null, Gc = !1, (t & 8) !== 0 && (t |= t & 32);
        var a = e.entangledLanes;
        if (a !== 0)
            for (e = e.entanglements, a &= t; 0 < a;) {
                var n = 31 - mt(a),
                    u = 1 << n;
                t |= e[n], a &= ~u
            }
        return el = t, Jn(), l
    }

    function Rr(e, t) {
        te = null, x.H = cn, t === ma || t === lu ? (t = Kf(), ge = 3) : t === Wi ? (t = Kf(), ge = 4) : ge = t === Tc ? 8 : t !== null && typeof t == "object" && typeof t.then == "function" ? 6 : 1, pt = t, ie === null && (He = 1, gu(e, xt(t, e.current)))
    }

    function Ur() {
        var e = gt.current;
        return e === null ? !0 : (fe & 4194048) === fe ? Dt === null : (fe & 62914560) === fe || (fe & 536870912) !== 0 ? e === Dt : !1
    }

    function Cr() {
        var e = x.H;
        return x.H = cn, e === null ? cn : e
    }

    function Hr() {
        var e = x.A;
        return x.A = Rh, e
    }

    function Du() {
        He = 4, gl || (fe & 4194048) !== fe && gt.current !== null || (Na = !0), (yl & 134217727) === 0 && (Zl & 134217727) === 0 || xe === null || bl(xe, fe, St, !1)
    }

    function Zc(e, t, l) {
        var a = he;
        he |= 2;
        var n = Cr(),
            u = Hr();
        (xe !== e || fe !== t) && (ju = null, xa(e, t)), t = !1;
        var i = He;
        e: do try {
                if (ge !== 0 && ie !== null) {
                    var s = ie,
                        r = pt;
                    switch (ge) {
                    case 8:
                        wc(), i = 6;
                        break e;
                    case 3:
                    case 2:
                    case 9:
                    case 6:
                        gt.current === null && (t = !0);
                        var y = ge;
                        if (ge = 0, pt = null, za(e, s, r, y), l && Na) {
                            i = 0;
                            break e
                        }
                        break;
                    default:
                        y = ge, ge = 0, pt = null, za(e, s, r, y)
                    }
                }
                Hh(), i = He;
                break
            } catch (T) {
                Rr(e, T)
            }
            while (!0);
            return t && e.shellSuspendCounter++, Vt = Bl = null, he = a, x.H = n, x.A = u, ie === null && (xe = null, fe = 0, Jn()), i
    }

    function Hh() {
        for (; ie !== null;) qr(ie)
    }

    function qh(e, t) {
        var l = he;
        he |= 2;
        var a = Cr(),
            n = Hr();
        xe !== e || fe !== t ? (ju = null, zu = rt() + 500, xa(e, t)) : Na = Ha(e, t);
        e: do try {
                if (ge !== 0 && ie !== null) {
                    t = ie;
                    var u = pt;
                    t: switch (ge) {
                    case 1:
                        ge = 0, pt = null, za(e, t, u, 1);
                        break;
                    case 2:
                    case 9:
                        if (wf(u)) {
                            ge = 0, pt = null, Br(t);
                            break
                        }
                        t = function () {
                            ge !== 2 && ge !== 9 || xe !== e || (ge = 7), Lt(e)
                        }, u.then(t, t);
                        break e;
                    case 3:
                        ge = 7;
                        break e;
                    case 4:
                        ge = 5;
                        break e;
                    case 7:
                        wf(u) ? (ge = 0, pt = null, Br(t)) : (ge = 0, pt = null, za(e, t, u, 7));
                        break;
                    case 5:
                        var i = null;
                        switch (ie.tag) {
                        case 26:
                            i = ie.memoizedState;
                        case 5:
                        case 27:
                            var s = ie;
                            if (i ? Ed(i) : s.stateNode.complete) {
                                ge = 0, pt = null;
                                var r = s.sibling;
                                if (r !== null) ie = r;
                                else {
                                    var y = s.return;
                                    y !== null ? (ie = y, Au(y)) : ie = null
                                }
                                break t
                            }
                        }
                        ge = 0, pt = null, za(e, t, u, 5);
                        break;
                    case 6:
                        ge = 0, pt = null, za(e, t, u, 6);
                        break;
                    case 8:
                        wc(), He = 6;
                        break e;
                    default:
                        throw Error(o(462))
                    }
                }
                Bh();
                break
            } catch (T) {
                Rr(e, T)
            }
            while (!0);
            return Vt = Bl = null, x.H = a, x.A = n, he = l, ie !== null ? 0 : (xe = null, fe = 0, Jn(), He)
    }

    function Bh() {
        for (; ie !== null && !im();) qr(ie)
    }

    function qr(e) {
        var t = ir(e.alternate, e, el);
        e.memoizedProps = e.pendingProps, t === null ? Au(e) : ie = t
    }

    function Br(e) {
        var t = e,
            l = t.alternate;
        switch (t.tag) {
        case 15:
        case 0:
            t = er(l, t, t.pendingProps, t.type, void 0, fe);
            break;
        case 11:
            t = er(l, t, t.pendingProps, t.type.render, t.ref, fe);
            break;
        case 5:
            cc(t);
        default:
            sr(l, t), t = ie = Cf(t, el), t = ir(l, t, el)
        }
        e.memoizedProps = e.pendingProps, t === null ? Au(e) : ie = t
    }

    function za(e, t, l, a) {
        Vt = Bl = null, cc(t), ha = null, Ia = 0;
        var n = t.return;
        try {
            if (zh(e, n, t, l, fe)) {
                He = 1, gu(e, xt(l, e.current)), ie = null;
                return
            }
        } catch (u) {
            if (n !== null) throw ie = n, u;
            He = 1, gu(e, xt(l, e.current)), ie = null;
            return
        }
        t.flags & 32768 ? (re || a === 1 ? e = !0 : Na || (fe & 536870912) !== 0 ? e = !1 : (gl = e = !0, (a === 2 || a === 9 || a === 3 || a === 6) && (a = gt.current, a !== null && a.tag === 13 && (a.flags |= 16384))), Lr(t, e)) : Au(t)
    }

    function Au(e) {
        var t = e;
        do {
            if ((t.flags & 32768) !== 0) {
                Lr(t, gl);
                return
            }
            e = t.return;
            var l = Dh(t.alternate, t, el);
            if (l !== null) {
                ie = l;
                return
            }
            if (t = t.sibling, t !== null) {
                ie = t;
                return
            }
            ie = t = e
        } while (t !== null);
        He === 0 && (He = 5)
    }

    function Lr(e, t) {
        do {
            var l = Ah(e.alternate, e);
            if (l !== null) {
                l.flags &= 32767, ie = l;
                return
            }
            if (l = e.return, l !== null && (l.flags |= 32768, l.subtreeFlags = 0, l.deletions = null), !t && (e = e.sibling, e !== null)) {
                ie = e;
                return
            }
            ie = e = l
        } while (e !== null);
        He = 6, ie = null
    }

    function kr(e, t, l, a, n, u, i, s, r) {
        e.cancelPendingCommit = null;
        do _u(); while (Qe !== 0);
        if ((he & 6) !== 0) throw Error(o(327));
        if (t !== null) {
            if (t === e.current) throw Error(o(177));
            if (u = t.lanes | t.childLanes, u |= Ci, gm(e, l, u, i, s, r), e === xe && (ie = xe = null, fe = 0), Ta = t, Sl = e, tl = l, Xc = u, Qc = n, Dr = a, (t.subtreeFlags & 10256) !== 0 || (t.flags & 10256) !== 0 ? (e.callbackNode = null, e.callbackPriority = 0, Gh(Rn, function () {
                    return Vr(), null
                })) : (e.callbackNode = null, e.callbackPriority = 0), a = (t.flags & 13878) !== 0, (t.subtreeFlags & 13878) !== 0 || a) {
                a = x.T, x.T = null, n = H.p, H.p = 2, i = he, he |= 4;
                try {
                    _h(e, t, l)
                } finally {
                    he = i, H.p = n, x.T = a
                }
            }
            Qe = 1, Yr(), Gr(), Xr()
        }
    }

    function Yr() {
        if (Qe === 1) {
            Qe = 0;
            var e = Sl,
                t = Ta,
                l = (t.flags & 13878) !== 0;
            if ((t.subtreeFlags & 13878) !== 0 || l) {
                l = x.T, x.T = null;
                var a = H.p;
                H.p = 2;
                var n = he;
                he |= 4;
                try {
                    br(t, e);
                    var u = ns,
                        i = zf(e.containerInfo),
                        s = u.focusedElem,
                        r = u.selectionRange;
                    if (i !== s && s && s.ownerDocument && xf(s.ownerDocument.documentElement, s)) {
                        if (r !== null && Ai(s)) {
                            var y = r.start,
                                T = r.end;
                            if (T === void 0 && (T = y), "selectionStart" in s) s.selectionStart = y, s.selectionEnd = Math.min(T, s.value.length);
                            else {
                                var D = s.ownerDocument || document,
                                    p = D && D.defaultView || window;
                                if (p.getSelection) {
                                    var E = p.getSelection(),
                                        k = s.textContent.length,
                                        $ = Math.min(r.start, k),
                                        Ee = r.end === void 0 ? $ : Math.min(r.end, k);
                                    !E.extend && $ > Ee && (i = Ee, Ee = $, $ = i);
                                    var v = Tf(s, $),
                                        d = Tf(s, Ee);
                                    if (v && d && (E.rangeCount !== 1 || E.anchorNode !== v.node || E.anchorOffset !== v.offset || E.focusNode !== d.node || E.focusOffset !== d.offset)) {
                                        var g = D.createRange();
                                        g.setStart(v.node, v.offset), E.removeAllRanges(), $ > Ee ? (E.addRange(g), E.extend(d.node, d.offset)) : (g.setEnd(d.node, d.offset), E.addRange(g))
                                    }
                                }
                            }
                        }
                        for (D = [], E = s; E = E.parentNode;) E.nodeType === 1 && D.push({
                            element: E,
                            left: E.scrollLeft,
                            top: E.scrollTop
                        });
                        for (typeof s.focus == "function" && s.focus(), s = 0; s < D.length; s++) {
                            var j = D[s];
                            j.element.scrollLeft = j.left, j.element.scrollTop = j.top
                        }
                    }
                    Xu = !!as, ns = as = null
                } finally {
                    he = n, H.p = a, x.T = l
                }
            }
            e.current = t, Qe = 2
        }
    }

    function Gr() {
        if (Qe === 2) {
            Qe = 0;
            var e = Sl,
                t = Ta,
                l = (t.flags & 8772) !== 0;
            if ((t.subtreeFlags & 8772) !== 0 || l) {
                l = x.T, x.T = null;
                var a = H.p;
                H.p = 2;
                var n = he;
                he |= 4;
                try {
                    vr(e, t.alternate, t)
                } finally {
                    he = n, H.p = a, x.T = l
                }
            }
            Qe = 3
        }
    }

    function Xr() {
        if (Qe === 4 || Qe === 3) {
            Qe = 0, cm();
            var e = Sl,
                t = Ta,
                l = tl,
                a = Dr;
            (t.subtreeFlags & 10256) !== 0 || (t.flags & 10256) !== 0 ? Qe = 5 : (Qe = 0, Ta = Sl = null, Qr(e, e.pendingLanes));
            var n = e.pendingLanes;
            if (n === 0 && (pl = null), oi(l), t = t.stateNode, dt && typeof dt.onCommitFiberRoot == "function") try {
                dt.onCommitFiberRoot(Ca, t, void 0, (t.current.flags & 128) === 128)
            } catch {}
            if (a !== null) {
                t = x.T, n = H.p, H.p = 2, x.T = null;
                try {
                    for (var u = e.onRecoverableError, i = 0; i < a.length; i++) {
                        var s = a[i];
                        u(s.value, {
                            componentStack: s.stack
                        })
                    }
                } finally {
                    x.T = t, H.p = n
                }
            }(tl & 3) !== 0 && _u(), Lt(e), n = e.pendingLanes, (l & 261930) !== 0 && (n & 42) !== 0 ? e === Vc ? gn++ : (gn = 0, Vc = e) : gn = 0, yn(0)
        }
    }

    function Qr(e, t) {
        (e.pooledCacheLanes &= t) === 0 && (t = e.pooledCache, t != null && (e.pooledCache = null, $a(t)))
    }

    function _u() {
        return Yr(), Gr(), Xr(), Vr()
    }

    function Vr() {
        if (Qe !== 5) return !1;
        var e = Sl,
            t = Xc;
        Xc = 0;
        var l = oi(tl),
            a = x.T,
            n = H.p;
        try {
            H.p = 32 > l ? 32 : l, x.T = null, l = Qc, Qc = null;
            var u = Sl,
                i = tl;
            if (Qe = 0, Ta = Sl = null, tl = 0, (he & 6) !== 0) throw Error(o(331));
            var s = he;
            if (he |= 4, zr(u.current), Er(u, u.current, i, l), he = s, yn(0, !1), dt && typeof dt.onPostCommitFiberRoot == "function") try {
                dt.onPostCommitFiberRoot(Ca, u)
            } catch {}
            return !0
        } finally {
            H.p = n, x.T = a, Qr(e, t)
        }
    }

    function wr(e, t, l) {
        t = xt(l, t), t = Ec(e.stateNode, t, 2), e = dl(e, t, 2), e !== null && (qa(e, 2), Lt(e))
    }

    function ye(e, t, l) {
        if (e.tag === 3) wr(e, e, l);
        else
            for (; t !== null;) {
                if (t.tag === 3) {
                    wr(t, e, l);
                    break
                } else if (t.tag === 1) {
                    var a = t.stateNode;
                    if (typeof t.type.getDerivedStateFromError == "function" || typeof a.componentDidCatch == "function" && (pl === null || !pl.has(a))) {
                        e = xt(l, e), l = Zo(2), a = dl(t, l, 2), a !== null && (Ko(l, a, t, e), qa(a, 2), Lt(a));
                        break
                    }
                }
                t = t.return
            }
    }

    function Kc(e, t, l) {
        var a = e.pingCache;
        if (a === null) {
            a = e.pingCache = new Uh;
            var n = new Set;
            a.set(t, n)
        } else n = a.get(t), n === void 0 && (n = new Set, a.set(t, n));
        n.has(l) || (kc = !0, n.add(l), e = Lh.bind(null, e, t, l), t.then(e, e))
    }

    function Lh(e, t, l) {
        var a = e.pingCache;
        a !== null && a.delete(t), e.pingedLanes |= e.suspendedLanes & l, e.warmLanes &= ~l, xe === e && (fe & l) === l && (He === 4 || He === 3 && (fe & 62914560) === fe && 300 > rt() - xu ? (he & 2) === 0 && xa(e, 0) : Yc |= l, Ea === fe && (Ea = 0)), Lt(e)
    }

    function Zr(e, t) {
        t === 0 && (t = Ls()), e = Cl(e, t), e !== null && (qa(e, t), Lt(e))
    }

    function kh(e) {
        var t = e.memoizedState,
            l = 0;
        t !== null && (l = t.retryLane), Zr(e, l)
    }

    function Yh(e, t) {
        var l = 0;
        switch (e.tag) {
        case 31:
        case 13:
            var a = e.stateNode,
                n = e.memoizedState;
            n !== null && (l = n.retryLane);
            break;
        case 19:
            a = e.stateNode;
            break;
        case 22:
            a = e.stateNode._retryCache;
            break;
        default:
            throw Error(o(314))
        }
        a !== null && a.delete(t), Zr(e, l)
    }

    function Gh(e, t) {
        return ii(e, t)
    }
    var Ou = null,
        ja = null,
        Jc = !1,
        Ru = !1,
        Wc = !1,
        Nl = 0;

    function Lt(e) {
        e !== ja && e.next === null && (ja === null ? Ou = ja = e : ja = ja.next = e), Ru = !0, Jc || (Jc = !0, Qh())
    }

    function yn(e, t) {
        if (!Wc && Ru) {
            Wc = !0;
            do
                for (var l = !1, a = Ou; a !== null;) {
                    if (e !== 0) {
                        var n = a.pendingLanes;
                        if (n === 0) var u = 0;
                        else {
                            var i = a.suspendedLanes,
                                s = a.pingedLanes;
                            u = (1 << 31 - mt(42 | e) + 1) - 1, u &= n & ~(i & ~s), u = u & 201326741 ? u & 201326741 | 1 : u ? u | 2 : 0
                        }
                        u !== 0 && (l = !0, $r(a, u))
                    } else u = fe, u = qn(a, a === xe ? u : 0, a.cancelPendingCommit !== null || a.timeoutHandle !== -1), (u & 3) === 0 || Ha(a, u) || (l = !0, $r(a, u));
                    a = a.next
                }
            while (l);
            Wc = !1
        }
    }

    function Xh() {
        Kr()
    }

    function Kr() {
        Ru = Jc = !1;
        var e = 0;
        Nl !== 0 && Ph() && (e = Nl);
        for (var t = rt(), l = null, a = Ou; a !== null;) {
            var n = a.next,
                u = Jr(a, t);
            u === 0 ? (a.next = null, l === null ? Ou = n : l.next = n, n === null && (ja = l)) : (l = a, (e !== 0 || (u & 3) !== 0) && (Ru = !0)), a = n
        }
        Qe !== 0 && Qe !== 5 || yn(e), Nl !== 0 && (Nl = 0)
    }

    function Jr(e, t) {
        for (var l = e.suspendedLanes, a = e.pingedLanes, n = e.expirationTimes, u = e.pendingLanes & -62914561; 0 < u;) {
            var i = 31 - mt(u),
                s = 1 << i,
                r = n[i];
            r === -1 ? ((s & l) === 0 || (s & a) !== 0) && (n[i] = vm(s, t)) : r <= t && (e.expiredLanes |= s), u &= ~s
        }
        if (t = xe, l = fe, l = qn(e, e === t ? l : 0, e.cancelPendingCommit !== null || e.timeoutHandle !== -1), a = e.callbackNode, l === 0 || e === t && (ge === 2 || ge === 9) || e.cancelPendingCommit !== null) return a !== null && a !== null && ci(a), e.callbackNode = null, e.callbackPriority = 0;
        if ((l & 3) === 0 || Ha(e, l)) {
            if (t = l & -l, t === e.callbackPriority) return t;
            switch (a !== null && ci(a), oi(l)) {
            case 2:
            case 8:
                l = qs;
                break;
            case 32:
                l = Rn;
                break;
            case 268435456:
                l = Bs;
                break;
            default:
                l = Rn
            }
            return a = Wr.bind(null, e), l = ii(l, a), e.callbackPriority = t, e.callbackNode = l, t
        }
        return a !== null && a !== null && ci(a), e.callbackPriority = 2, e.callbackNode = null, 2
    }

    function Wr(e, t) {
        if (Qe !== 0 && Qe !== 5) return e.callbackNode = null, e.callbackPriority = 0, null;
        var l = e.callbackNode;
        if (_u() && e.callbackNode !== l) return null;
        var a = fe;
        return a = qn(e, e === xe ? a : 0, e.cancelPendingCommit !== null || e.timeoutHandle !== -1), a === 0 ? null : (_r(e, a, t), Jr(e, rt()), e.callbackNode != null && e.callbackNode === l ? Wr.bind(null, e) : null)
    }

    function $r(e, t) {
        if (_u()) return null;
        _r(e, t, !0)
    }

    function Qh() {
        t1(function () {
            (he & 6) !== 0 ? ii(Hs, Xh) : Kr()
        })
    }

    function $c() {
        if (Nl === 0) {
            var e = ra;
            e === 0 && (e = Un, Un <<= 1, (Un & 261888) === 0 && (Un = 256)), Nl = e
        }
        return Nl
    }

    function Fr(e) {
        return e == null || typeof e == "symbol" || typeof e == "boolean" ? null : typeof e == "function" ? e : Yn("" + e)
    }

    function Ir(e, t) {
        var l = t.ownerDocument.createElement("input");
        return l.name = t.name, l.value = t.value, e.id && l.setAttribute("form", e.id), t.parentNode.insertBefore(l, t), e = new FormData(e), l.parentNode.removeChild(l), e
    }

    function Vh(e, t, l, a, n) {
        if (t === "submit" && l && l.stateNode === n) {
            var u = Fr((n[at] || null).action),
                i = a.submitter;
            i && (t = (t = i[at] || null) ? Fr(t.formAction) : i.getAttribute("formAction"), t !== null && (u = t, i = null));
            var s = new Vn("action", "action", null, a, n);
            e.push({
                event: s,
                listeners: [{
                    instance: null,
                    listener: function () {
                        if (a.defaultPrevented) {
                            if (Nl !== 0) {
                                var r = i ? Ir(n, i) : new FormData(n);
                                gc(l, {
                                    pending: !0,
                                    data: r,
                                    method: n.method,
                                    action: u
                                }, null, r)
                            }
                        } else typeof u == "function" && (s.preventDefault(), r = i ? Ir(n, i) : new FormData(n), gc(l, {
                            pending: !0,
                            data: r,
                            method: n.method,
                            action: u
                        }, u, r))
                    },
                    currentTarget: n
                }]
            })
        }
    }
    for (var Fc = 0; Fc < Ui.length; Fc++) {
        var Ic = Ui[Fc],
            wh = Ic.toLowerCase(),
            Zh = Ic[0].toUpperCase() + Ic.slice(1);
        Ot(wh, "on" + Zh)
    }
    Ot(Df, "onAnimationEnd"), Ot(Af, "onAnimationIteration"), Ot(_f, "onAnimationStart"), Ot("dblclick", "onDoubleClick"), Ot("focusin", "onFocus"), Ot("focusout", "onBlur"), Ot(sh, "onTransitionRun"), Ot(fh, "onTransitionStart"), Ot(oh, "onTransitionCancel"), Ot(Of, "onTransitionEnd"), Fl("onMouseEnter", ["mouseout", "mouseover"]), Fl("onMouseLeave", ["mouseout", "mouseover"]), Fl("onPointerEnter", ["pointerout", "pointerover"]), Fl("onPointerLeave", ["pointerout", "pointerover"]), _l("onChange", "change click focusin focusout input keydown keyup selectionchange".split(" ")), _l("onSelect", "focusout contextmenu dragend focusin keydown keyup mousedown mouseup selectionchange".split(" ")), _l("onBeforeInput", ["compositionend", "keypress", "textInput", "paste"]), _l("onCompositionEnd", "compositionend focusout keydown keypress keyup mousedown".split(" ")), _l("onCompositionStart", "compositionstart focusout keydown keypress keyup mousedown".split(" ")), _l("onCompositionUpdate", "compositionupdate focusout keydown keypress keyup mousedown".split(" "));
    var pn = "abort canplay canplaythrough durationchange emptied encrypted ended error loadeddata loadedmetadata loadstart pause play playing progress ratechange resize seeked seeking stalled suspend timeupdate volumechange waiting".split(" "),
        Kh = new Set("beforetoggle cancel close invalid load scroll scrollend toggle".split(" ").concat(pn));

    function Pr(e, t) {
        t = (t & 4) !== 0;
        for (var l = 0; l < e.length; l++) {
            var a = e[l],
                n = a.event;
            a = a.listeners;
            e: {
                var u = void 0;
                if (t)
                    for (var i = a.length - 1; 0 <= i; i--) {
                        var s = a[i],
                            r = s.instance,
                            y = s.currentTarget;
                        if (s = s.listener, r !== u && n.isPropagationStopped()) break e;
                        u = s, n.currentTarget = y;
                        try {
                            u(n)
                        } catch (T) {
                            Kn(T)
                        }
                        n.currentTarget = null, u = r
                    } else
                        for (i = 0; i < a.length; i++) {
                            if (s = a[i], r = s.instance, y = s.currentTarget, s = s.listener, r !== u && n.isPropagationStopped()) break e;
                            u = s, n.currentTarget = y;
                            try {
                                u(n)
                            } catch (T) {
                                Kn(T)
                            }
                            n.currentTarget = null, u = r
                        }
            }
        }
    }

    function ce(e, t) {
        var l = t[ri];
        l === void 0 && (l = t[ri] = new Set);
        var a = e + "__bubble";
        l.has(a) || (ed(t, e, 2, !1), l.add(a))
    }

    function Pc(e, t, l) {
        var a = 0;
        t && (a |= 4), ed(l, e, a, t)
    }
    var Uu = "_reactListening" + Math.random().toString(36).slice(2);

    function es(e) {
        if (!e[Uu]) {
            e[Uu] = !0, ws.forEach(function (l) {
                l !== "selectionchange" && (Kh.has(l) || Pc(l, !1, e), Pc(l, !0, e))
            });
            var t = e.nodeType === 9 ? e : e.ownerDocument;
            t === null || t[Uu] || (t[Uu] = !0, Pc("selectionchange", !1, t))
        }
    }

    function ed(e, t, l, a) {
        switch (Ad(t)) {
        case 2:
            var n = N1;
            break;
        case 8:
            n = E1;
            break;
        default:
            n = vs
        }
        l = n.bind(null, t, l, e), n = void 0, !bi || t !== "touchstart" && t !== "touchmove" && t !== "wheel" || (n = !0), a ? n !== void 0 ? e.addEventListener(t, l, {
            capture: !0,
            passive: n
        }) : e.addEventListener(t, l, !0) : n !== void 0 ? e.addEventListener(t, l, {
            passive: n
        }) : e.addEventListener(t, l, !1)
    }

    function ts(e, t, l, a, n) {
        var u = a;
        if ((t & 1) === 0 && (t & 2) === 0 && a !== null) e: for (;;) {
            if (a === null) return;
            var i = a.tag;
            if (i === 3 || i === 4) {
                var s = a.stateNode.containerInfo;
                if (s === n) break;
                if (i === 4)
                    for (i = a.return; i !== null;) {
                        var r = i.tag;
                        if ((r === 3 || r === 4) && i.stateNode.containerInfo === n) return;
                        i = i.return
                    }
                for (; s !== null;) {
                    if (i = Jl(s), i === null) return;
                    if (r = i.tag, r === 5 || r === 6 || r === 26 || r === 27) {
                        a = u = i;
                        continue e
                    }
                    s = s.parentNode
                }
            }
            a = a.return
        }
        af(function () {
            var y = u,
                T = pi(l),
                D = [];
            e: {
                var p = Rf.get(e);
                if (p !== void 0) {
                    var E = Vn,
                        k = e;
                    switch (e) {
                    case "keypress":
                        if (Xn(l) === 0) break e;
                    case "keydown":
                    case "keyup":
                        E = Ym;
                        break;
                    case "focusin":
                        k = "focus", E = xi;
                        break;
                    case "focusout":
                        k = "blur", E = xi;
                        break;
                    case "beforeblur":
                    case "afterblur":
                        E = xi;
                        break;
                    case "click":
                        if (l.button === 2) break e;
                    case "auxclick":
                    case "dblclick":
                    case "mousedown":
                    case "mousemove":
                    case "mouseup":
                    case "mouseout":
                    case "mouseover":
                    case "contextmenu":
                        E = cf;
                        break;
                    case "drag":
                    case "dragend":
                    case "dragenter":
                    case "dragexit":
                    case "dragleave":
                    case "dragover":
                    case "dragstart":
                    case "drop":
                        E = Dm;
                        break;
                    case "touchcancel":
                    case "touchend":
                    case "touchmove":
                    case "touchstart":
                        E = Qm;
                        break;
                    case Df:
                    case Af:
                    case _f:
                        E = Om;
                        break;
                    case Of:
                        E = wm;
                        break;
                    case "scroll":
                    case "scrollend":
                        E = jm;
                        break;
                    case "wheel":
                        E = Km;
                        break;
                    case "copy":
                    case "cut":
                    case "paste":
                        E = Um;
                        break;
                    case "gotpointercapture":
                    case "lostpointercapture":
                    case "pointercancel":
                    case "pointerdown":
                    case "pointermove":
                    case "pointerout":
                    case "pointerover":
                    case "pointerup":
                        E = ff;
                        break;
                    case "toggle":
                    case "beforetoggle":
                        E = Wm
                    }
                    var $ = (t & 4) !== 0,
                        Ee = !$ && (e === "scroll" || e === "scrollend"),
                        v = $ ? p !== null ? p + "Capture" : null : p;
                    $ = [];
                    for (var d = y, g; d !== null;) {
                        var j = d;
                        if (g = j.stateNode, j = j.tag, j !== 5 && j !== 26 && j !== 27 || g === null || v === null || (j = ka(d, v), j != null && $.push(Sn(d, j, g))), Ee) break;
                        d = d.return
                    }
                    0 < $.length && (p = new E(p, k, null, l, T), D.push({
                        event: p,
                        listeners: $
                    }))
                }
            }
            if ((t & 7) === 0) {
                e: {
                    if (p = e === "mouseover" || e === "pointerover", E = e === "mouseout" || e === "pointerout", p && l !== yi && (k = l.relatedTarget || l.fromElement) && (Jl(k) || k[Kl])) break e;
                    if ((E || p) && (p = T.window === T ? T : (p = T.ownerDocument) ? p.defaultView || p.parentWindow : window, E ? (k = l.relatedTarget || l.toElement, E = y, k = k ? Jl(k) : null, k !== null && (Ee = z(k), $ = k.tag, k !== Ee || $ !== 5 && $ !== 27 && $ !== 6) && (k = null)) : (E = null, k = y), E !== k)) {
                        if ($ = cf, j = "onMouseLeave", v = "onMouseEnter", d = "mouse", (e === "pointerout" || e === "pointerover") && ($ = ff, j = "onPointerLeave", v = "onPointerEnter", d = "pointer"), Ee = E == null ? p : La(E), g = k == null ? p : La(k), p = new $(j, d + "leave", E, l, T), p.target = Ee, p.relatedTarget = g, j = null, Jl(T) === y && ($ = new $(v, d + "enter", k, l, T), $.target = g, $.relatedTarget = Ee, j = $), Ee = j, E && k) t: {
                            for ($ = Jh, v = E, d = k, g = 0, j = v; j; j = $(j)) g++;j = 0;
                            for (var Z = d; Z; Z = $(Z)) j++;
                            for (; 0 < g - j;) v = $(v),
                            g--;
                            for (; 0 < j - g;) d = $(d),
                            j--;
                            for (; g--;) {
                                if (v === d || d !== null && v === d.alternate) {
                                    $ = v;
                                    break t
                                }
                                v = $(v), d = $(d)
                            }
                            $ = null
                        }
                        else $ = null;
                        E !== null && td(D, p, E, $, !1), k !== null && Ee !== null && td(D, Ee, k, $, !0)
                    }
                }
                e: {
                    if (p = y ? La(y) : window, E = p.nodeName && p.nodeName.toLowerCase(), E === "select" || E === "input" && p.type === "file") var de = yf;
                    else if (vf(p))
                        if (pf) de = uh;
                        else {
                            de = ah;
                            var G = lh
                        }
                    else E = p.nodeName,
                    !E || E.toLowerCase() !== "input" || p.type !== "checkbox" && p.type !== "radio" ? y && gi(y.elementType) && (de = yf) : de = nh;
                    if (de && (de = de(e, y))) {
                        gf(D, de, l, T);
                        break e
                    }
                    G && G(e, p, y),
                    e === "focusout" && y && p.type === "number" && y.memoizedProps.value != null && vi(p, "number", p.value)
                }
                switch (G = y ? La(y) : window, e) {
                case "focusin":
                    (vf(G) || G.contentEditable === "true") && (aa = G, _i = y, Ka = null);
                    break;
                case "focusout":
                    Ka = _i = aa = null;
                    break;
                case "mousedown":
                    Oi = !0;
                    break;
                case "contextmenu":
                case "mouseup":
                case "dragend":
                    Oi = !1, jf(D, l, T);
                    break;
                case "selectionchange":
                    if (ch) break;
                case "keydown":
                case "keyup":
                    jf(D, l, T)
                }
                var le;
                if (ji) e: {
                    switch (e) {
                    case "compositionstart":
                        var oe = "onCompositionStart";
                        break e;
                    case "compositionend":
                        oe = "onCompositionEnd";
                        break e;
                    case "compositionupdate":
                        oe = "onCompositionUpdate";
                        break e
                    }
                    oe = void 0
                }
                else la ? mf(e, l) && (oe = "onCompositionEnd") : e === "keydown" && l.keyCode === 229 && (oe = "onCompositionStart");oe && ( of && l.locale !== "ko" && (la || oe !== "onCompositionStart" ? oe === "onCompositionEnd" && la && (le = nf()) : (ul = T, Ni = "value" in ul ? ul.value : ul.textContent, la = !0)), G = Cu(y, oe), 0 < G.length && (oe = new sf(oe, e, null, l, T), D.push({
                    event: oe,
                    listeners: G
                }), le ? oe.data = le : (le = hf(l), le !== null && (oe.data = le)))),
                (le = Fm ? Im(e, l) : Pm(e, l)) && (oe = Cu(y, "onBeforeInput"), 0 < oe.length && (G = new sf("onBeforeInput", "beforeinput", null, l, T), D.push({
                    event: G,
                    listeners: oe
                }), G.data = le)),
                Vh(D, e, y, l, T)
            }
            Pr(D, t)
        })
    }

    function Sn(e, t, l) {
        return {
            instance: e,
            listener: t,
            currentTarget: l
        }
    }

    function Cu(e, t) {
        for (var l = t + "Capture", a = []; e !== null;) {
            var n = e,
                u = n.stateNode;
            if (n = n.tag, n !== 5 && n !== 26 && n !== 27 || u === null || (n = ka(e, l), n != null && a.unshift(Sn(e, n, u)), n = ka(e, t), n != null && a.push(Sn(e, n, u))), e.tag === 3) return a;
            e = e.return
        }
        return []
    }

    function Jh(e) {
        if (e === null) return null;
        do e = e.return; while (e && e.tag !== 5 && e.tag !== 27);
        return e || null
    }

    function td(e, t, l, a, n) {
        for (var u = t._reactName, i = []; l !== null && l !== a;) {
            var s = l,
                r = s.alternate,
                y = s.stateNode;
            if (s = s.tag, r !== null && r === a) break;
            s !== 5 && s !== 26 && s !== 27 || y === null || (r = y, n ? (y = ka(l, u), y != null && i.unshift(Sn(l, y, r))) : n || (y = ka(l, u), y != null && i.push(Sn(l, y, r)))), l = l.return
        }
        i.length !== 0 && e.push({
            event: t,
            listeners: i
        })
    }
    var Wh = /\r\n?/g,
        $h = /\u0000|\uFFFD/g;

    function ld(e) {
        return (typeof e == "string" ? e : "" + e).replace(Wh, `
`).replace($h, "")
    }

    function ad(e, t) {
        return t = ld(t), ld(e) === t
    }

    function Ne(e, t, l, a, n, u) {
        switch (l) {
        case "children":
            typeof a == "string" ? t === "body" || t === "textarea" && a === "" || Pl(e, a) : (typeof a == "number" || typeof a == "bigint") && t !== "body" && Pl(e, "" + a);
            break;
        case "className":
            Ln(e, "class", a);
            break;
        case "tabIndex":
            Ln(e, "tabindex", a);
            break;
        case "dir":
        case "role":
        case "viewBox":
        case "width":
        case "height":
            Ln(e, l, a);
            break;
        case "style":
            tf(e, a, u);
            break;
        case "data":
            if (t !== "object") {
                Ln(e, "data", a);
                break
            }
            case "src":
            case "href":
                if (a === "" && (t !== "a" || l !== "href")) {
                    e.removeAttribute(l);
                    break
                }
                if (a == null || typeof a == "function" || typeof a == "symbol" || typeof a == "boolean") {
                    e.removeAttribute(l);
                    break
                }
                a = Yn("" + a), e.setAttribute(l, a);
                break;
            case "action":
            case "formAction":
                if (typeof a == "function") {
                    e.setAttribute(l, "javascript:throw new Error('A React form was unexpectedly submitted. If you called form.submit() manually, consider using form.requestSubmit() instead. If you\\'re trying to use event.stopPropagation() in a submit event handler, consider also calling event.preventDefault().')");
                    break
                } else typeof u == "function" && (l === "formAction" ? (t !== "input" && Ne(e, t, "name", n.name, n, null), Ne(e, t, "formEncType", n.formEncType, n, null), Ne(e, t, "formMethod", n.formMethod, n, null), Ne(e, t, "formTarget", n.formTarget, n, null)) : (Ne(e, t, "encType", n.encType, n, null), Ne(e, t, "method", n.method, n, null), Ne(e, t, "target", n.target, n, null)));
                if (a == null || typeof a == "symbol" || typeof a == "boolean") {
                    e.removeAttribute(l);
                    break
                }
                a = Yn("" + a), e.setAttribute(l, a);
                break;
            case "onClick":
                a != null && (e.onclick = Yt);
                break;
            case "onScroll":
                a != null && ce("scroll", e);
                break;
            case "onScrollEnd":
                a != null && ce("scrollend", e);
                break;
            case "dangerouslySetInnerHTML":
                if (a != null) {
                    if (typeof a != "object" || !("__html" in a)) throw Error(o(61));
                    if (l = a.__html, l != null) {
                        if (n.children != null) throw Error(o(60));
                        e.innerHTML = l
                    }
                }
                break;
            case "multiple":
                e.multiple = a && typeof a != "function" && typeof a != "symbol";
                break;
            case "muted":
                e.muted = a && typeof a != "function" && typeof a != "symbol";
                break;
            case "suppressContentEditableWarning":
            case "suppressHydrationWarning":
            case "defaultValue":
            case "defaultChecked":
            case "innerHTML":
            case "ref":
                break;
            case "autoFocus":
                break;
            case "xlinkHref":
                if (a == null || typeof a == "function" || typeof a == "boolean" || typeof a == "symbol") {
                    e.removeAttribute("xlink:href");
                    break
                }
                l = Yn("" + a), e.setAttributeNS("http://www.w3.org/1999/xlink", "xlink:href", l);
                break;
            case "contentEditable":
            case "spellCheck":
            case "draggable":
            case "value":
            case "autoReverse":
            case "externalResourcesRequired":
            case "focusable":
            case "preserveAlpha":
                a != null && typeof a != "function" && typeof a != "symbol" ? e.setAttribute(l, "" + a) : e.removeAttribute(l);
                break;
            case "inert":
            case "allowFullScreen":
            case "async":
            case "autoPlay":
            case "controls":
            case "default":
            case "defer":
            case "disabled":
            case "disablePictureInPicture":
            case "disableRemotePlayback":
            case "formNoValidate":
            case "hidden":
            case "loop":
            case "noModule":
            case "noValidate":
            case "open":
            case "playsInline":
            case "readOnly":
            case "required":
            case "reversed":
            case "scoped":
            case "seamless":
            case "itemScope":
                a && typeof a != "function" && typeof a != "symbol" ? e.setAttribute(l, "") : e.removeAttribute(l);
                break;
            case "capture":
            case "download":
                a === !0 ? e.setAttribute(l, "") : a !== !1 && a != null && typeof a != "function" && typeof a != "symbol" ? e.setAttribute(l, a) : e.removeAttribute(l);
                break;
            case "cols":
            case "rows":
            case "size":
            case "span":
                a != null && typeof a != "function" && typeof a != "symbol" && !isNaN(a) && 1 <= a ? e.setAttribute(l, a) : e.removeAttribute(l);
                break;
            case "rowSpan":
            case "start":
                a == null || typeof a == "function" || typeof a == "symbol" || isNaN(a) ? e.removeAttribute(l) : e.setAttribute(l, a);
                break;
            case "popover":
                ce("beforetoggle", e), ce("toggle", e), Bn(e, "popover", a);
                break;
            case "xlinkActuate":
                kt(e, "http://www.w3.org/1999/xlink", "xlink:actuate", a);
                break;
            case "xlinkArcrole":
                kt(e, "http://www.w3.org/1999/xlink", "xlink:arcrole", a);
                break;
            case "xlinkRole":
                kt(e, "http://www.w3.org/1999/xlink", "xlink:role", a);
                break;
            case "xlinkShow":
                kt(e, "http://www.w3.org/1999/xlink", "xlink:show", a);
                break;
            case "xlinkTitle":
                kt(e, "http://www.w3.org/1999/xlink", "xlink:title", a);
                break;
            case "xlinkType":
                kt(e, "http://www.w3.org/1999/xlink", "xlink:type", a);
                break;
            case "xmlBase":
                kt(e, "http://www.w3.org/XML/1998/namespace", "xml:base", a);
                break;
            case "xmlLang":
                kt(e, "http://www.w3.org/XML/1998/namespace", "xml:lang", a);
                break;
            case "xmlSpace":
                kt(e, "http://www.w3.org/XML/1998/namespace", "xml:space", a);
                break;
            case "is":
                Bn(e, "is", a);
                break;
            case "innerText":
            case "textContent":
                break;
            default:
                (!(2 < l.length) || l[0] !== "o" && l[0] !== "O" || l[1] !== "n" && l[1] !== "N") && (l = xm.get(l) || l, Bn(e, l, a))
        }
    }

    function ls(e, t, l, a, n, u) {
        switch (l) {
        case "style":
            tf(e, a, u);
            break;
        case "dangerouslySetInnerHTML":
            if (a != null) {
                if (typeof a != "object" || !("__html" in a)) throw Error(o(61));
                if (l = a.__html, l != null) {
                    if (n.children != null) throw Error(o(60));
                    e.innerHTML = l
                }
            }
            break;
        case "children":
            typeof a == "string" ? Pl(e, a) : (typeof a == "number" || typeof a == "bigint") && Pl(e, "" + a);
            break;
        case "onScroll":
            a != null && ce("scroll", e);
            break;
        case "onScrollEnd":
            a != null && ce("scrollend", e);
            break;
        case "onClick":
            a != null && (e.onclick = Yt);
            break;
        case "suppressContentEditableWarning":
        case "suppressHydrationWarning":
        case "innerHTML":
        case "ref":
            break;
        case "innerText":
        case "textContent":
            break;
        default:
            if (!Zs.hasOwnProperty(l)) e: {
                if (l[0] === "o" && l[1] === "n" && (n = l.endsWith("Capture"), t = l.slice(2, n ? l.length - 7 : void 0), u = e[at] || null, u = u != null ? u[l] : null, typeof u == "function" && e.removeEventListener(t, u, n), typeof a == "function")) {
                    typeof u != "function" && u !== null && (l in e ? e[l] = null : e.hasAttribute(l) && e.removeAttribute(l)), e.addEventListener(t, a, n);
                    break e
                }
                l in e ? e[l] = a : a === !0 ? e.setAttribute(l, "") : Bn(e, l, a)
            }
        }
    }

    function Fe(e, t, l) {
        switch (t) {
        case "div":
        case "span":
        case "svg":
        case "path":
        case "a":
        case "g":
        case "p":
        case "li":
            break;
        case "img":
            ce("error", e), ce("load", e);
            var a = !1,
                n = !1,
                u;
            for (u in l)
                if (l.hasOwnProperty(u)) {
                    var i = l[u];
                    if (i != null) switch (u) {
                    case "src":
                        a = !0;
                        break;
                    case "srcSet":
                        n = !0;
                        break;
                    case "children":
                    case "dangerouslySetInnerHTML":
                        throw Error(o(137, t));
                    default:
                        Ne(e, t, u, i, l, null)
                    }
                } n && Ne(e, t, "srcSet", l.srcSet, l, null), a && Ne(e, t, "src", l.src, l, null);
            return;
        case "input":
            ce("invalid", e);
            var s = u = i = n = null,
                r = null,
                y = null;
            for (a in l)
                if (l.hasOwnProperty(a)) {
                    var T = l[a];
                    if (T != null) switch (a) {
                    case "name":
                        n = T;
                        break;
                    case "type":
                        i = T;
                        break;
                    case "checked":
                        r = T;
                        break;
                    case "defaultChecked":
                        y = T;
                        break;
                    case "value":
                        u = T;
                        break;
                    case "defaultValue":
                        s = T;
                        break;
                    case "children":
                    case "dangerouslySetInnerHTML":
                        if (T != null) throw Error(o(137, t));
                        break;
                    default:
                        Ne(e, t, a, T, l, null)
                    }
                } Fs(e, u, s, r, y, i, n, !1);
            return;
        case "select":
            ce("invalid", e), a = i = u = null;
            for (n in l)
                if (l.hasOwnProperty(n) && (s = l[n], s != null)) switch (n) {
                case "value":
                    u = s;
                    break;
                case "defaultValue":
                    i = s;
                    break;
                case "multiple":
                    a = s;
                default:
                    Ne(e, t, n, s, l, null)
                }
            t = u, l = i, e.multiple = !!a, t != null ? Il(e, !!a, t, !1) : l != null && Il(e, !!a, l, !0);
            return;
        case "textarea":
            ce("invalid", e), u = n = a = null;
            for (i in l)
                if (l.hasOwnProperty(i) && (s = l[i], s != null)) switch (i) {
                case "value":
                    a = s;
                    break;
                case "defaultValue":
                    n = s;
                    break;
                case "children":
                    u = s;
                    break;
                case "dangerouslySetInnerHTML":
                    if (s != null) throw Error(o(91));
                    break;
                default:
                    Ne(e, t, i, s, l, null)
                }
            Ps(e, a, n, u);
            return;
        case "option":
            for (r in l) l.hasOwnProperty(r) && (a = l[r], a != null) && (r === "selected" ? e.selected = a && typeof a != "function" && typeof a != "symbol" : Ne(e, t, r, a, l, null));
            return;
        case "dialog":
            ce("beforetoggle", e), ce("toggle", e), ce("cancel", e), ce("close", e);
            break;
        case "iframe":
        case "object":
            ce("load", e);
            break;
        case "video":
        case "audio":
            for (a = 0; a < pn.length; a++) ce(pn[a], e);
            break;
        case "image":
            ce("error", e), ce("load", e);
            break;
        case "details":
            ce("toggle", e);
            break;
        case "embed":
        case "source":
        case "link":
            ce("error", e), ce("load", e);
        case "area":
        case "base":
        case "br":
        case "col":
        case "hr":
        case "keygen":
        case "meta":
        case "param":
        case "track":
        case "wbr":
        case "menuitem":
            for (y in l)
                if (l.hasOwnProperty(y) && (a = l[y], a != null)) switch (y) {
                case "children":
                case "dangerouslySetInnerHTML":
                    throw Error(o(137, t));
                default:
                    Ne(e, t, y, a, l, null)
                }
            return;
        default:
            if (gi(t)) {
                for (T in l) l.hasOwnProperty(T) && (a = l[T], a !== void 0 && ls(e, t, T, a, l, void 0));
                return
            }
        }
        for (s in l) l.hasOwnProperty(s) && (a = l[s], a != null && Ne(e, t, s, a, l, null))
    }

    function Fh(e, t, l, a) {
        switch (t) {
        case "div":
        case "span":
        case "svg":
        case "path":
        case "a":
        case "g":
        case "p":
        case "li":
            break;
        case "input":
            var n = null,
                u = null,
                i = null,
                s = null,
                r = null,
                y = null,
                T = null;
            for (E in l) {
                var D = l[E];
                if (l.hasOwnProperty(E) && D != null) switch (E) {
                case "checked":
                    break;
                case "value":
                    break;
                case "defaultValue":
                    r = D;
                default:
                    a.hasOwnProperty(E) || Ne(e, t, E, null, a, D)
                }
            }
            for (var p in a) {
                var E = a[p];
                if (D = l[p], a.hasOwnProperty(p) && (E != null || D != null)) switch (p) {
                case "type":
                    u = E;
                    break;
                case "name":
                    n = E;
                    break;
                case "checked":
                    y = E;
                    break;
                case "defaultChecked":
                    T = E;
                    break;
                case "value":
                    i = E;
                    break;
                case "defaultValue":
                    s = E;
                    break;
                case "children":
                case "dangerouslySetInnerHTML":
                    if (E != null) throw Error(o(137, t));
                    break;
                default:
                    E !== D && Ne(e, t, p, E, a, D)
                }
            }
            hi(e, i, s, r, y, T, u, n);
            return;
        case "select":
            E = i = s = p = null;
            for (u in l)
                if (r = l[u], l.hasOwnProperty(u) && r != null) switch (u) {
                case "value":
                    break;
                case "multiple":
                    E = r;
                default:
                    a.hasOwnProperty(u) || Ne(e, t, u, null, a, r)
                }
            for (n in a)
                if (u = a[n], r = l[n], a.hasOwnProperty(n) && (u != null || r != null)) switch (n) {
                case "value":
                    p = u;
                    break;
                case "defaultValue":
                    s = u;
                    break;
                case "multiple":
                    i = u;
                default:
                    u !== r && Ne(e, t, n, u, a, r)
                }
            t = s, l = i, a = E, p != null ? Il(e, !!l, p, !1) : !!a != !!l && (t != null ? Il(e, !!l, t, !0) : Il(e, !!l, l ? [] : "", !1));
            return;
        case "textarea":
            E = p = null;
            for (s in l)
                if (n = l[s], l.hasOwnProperty(s) && n != null && !a.hasOwnProperty(s)) switch (s) {
                case "value":
                    break;
                case "children":
                    break;
                default:
                    Ne(e, t, s, null, a, n)
                }
            for (i in a)
                if (n = a[i], u = l[i], a.hasOwnProperty(i) && (n != null || u != null)) switch (i) {
                case "value":
                    p = n;
                    break;
                case "defaultValue":
                    E = n;
                    break;
                case "children":
                    break;
                case "dangerouslySetInnerHTML":
                    if (n != null) throw Error(o(91));
                    break;
                default:
                    n !== u && Ne(e, t, i, n, a, u)
                }
            Is(e, p, E);
            return;
        case "option":
            for (var k in l) p = l[k], l.hasOwnProperty(k) && p != null && !a.hasOwnProperty(k) && (k === "selected" ? e.selected = !1 : Ne(e, t, k, null, a, p));
            for (r in a) p = a[r], E = l[r], a.hasOwnProperty(r) && p !== E && (p != null || E != null) && (r === "selected" ? e.selected = p && typeof p != "function" && typeof p != "symbol" : Ne(e, t, r, p, a, E));
            return;
        case "img":
        case "link":
        case "area":
        case "base":
        case "br":
        case "col":
        case "embed":
        case "hr":
        case "keygen":
        case "meta":
        case "param":
        case "source":
        case "track":
        case "wbr":
        case "menuitem":
            for (var $ in l) p = l[$], l.hasOwnProperty($) && p != null && !a.hasOwnProperty($) && Ne(e, t, $, null, a, p);
            for (y in a)
                if (p = a[y], E = l[y], a.hasOwnProperty(y) && p !== E && (p != null || E != null)) switch (y) {
                case "children":
                case "dangerouslySetInnerHTML":
                    if (p != null) throw Error(o(137, t));
                    break;
                default:
                    Ne(e, t, y, p, a, E)
                }
            return;
        default:
            if (gi(t)) {
                for (var Ee in l) p = l[Ee], l.hasOwnProperty(Ee) && p !== void 0 && !a.hasOwnProperty(Ee) && ls(e, t, Ee, void 0, a, p);
                for (T in a) p = a[T], E = l[T], !a.hasOwnProperty(T) || p === E || p === void 0 && E === void 0 || ls(e, t, T, p, a, E);
                return
            }
        }
        for (var v in l) p = l[v], l.hasOwnProperty(v) && p != null && !a.hasOwnProperty(v) && Ne(e, t, v, null, a, p);
        for (D in a) p = a[D], E = l[D], !a.hasOwnProperty(D) || p === E || p == null && E == null || Ne(e, t, D, p, a, E)
    }

    function nd(e) {
        switch (e) {
        case "css":
        case "script":
        case "font":
        case "img":
        case "image":
        case "input":
        case "link":
            return !0;
        default:
            return !1
        }
    }

    function Ih() {
        if (typeof performance.getEntriesByType == "function") {
            for (var e = 0, t = 0, l = performance.getEntriesByType("resource"), a = 0; a < l.length; a++) {
                var n = l[a],
                    u = n.transferSize,
                    i = n.initiatorType,
                    s = n.duration;
                if (u && s && nd(i)) {
                    for (i = 0, s = n.responseEnd, a += 1; a < l.length; a++) {
                        var r = l[a],
                            y = r.startTime;
                        if (y > s) break;
                        var T = r.transferSize,
                            D = r.initiatorType;
                        T && nd(D) && (r = r.responseEnd, i += T * (r < s ? 1 : (s - y) / (r - y)))
                    }
                    if (--a, t += 8 * (u + i) / (n.duration / 1e3), e++, 10 < e) break
                }
            }
            if (0 < e) return t / e / 1e6
        }
        return navigator.connection && (e = navigator.connection.downlink, typeof e == "number") ? e : 5
    }
    var as = null,
        ns = null;

    function Hu(e) {
        return e.nodeType === 9 ? e : e.ownerDocument
    }

    function ud(e) {
        switch (e) {
        case "http://www.w3.org/2000/svg":
            return 1;
        case "http://www.w3.org/1998/Math/MathML":
            return 2;
        default:
            return 0
        }
    }

    function id(e, t) {
        if (e === 0) switch (t) {
        case "svg":
            return 1;
        case "math":
            return 2;
        default:
            return 0
        }
        return e === 1 && t === "foreignObject" ? 0 : e
    }

    function us(e, t) {
        return e === "textarea" || e === "noscript" || typeof t.children == "string" || typeof t.children == "number" || typeof t.children == "bigint" || typeof t.dangerouslySetInnerHTML == "object" && t.dangerouslySetInnerHTML !== null && t.dangerouslySetInnerHTML.__html != null
    }
    var is = null;

    function Ph() {
        var e = window.event;
        return e && e.type === "popstate" ? e === is ? !1 : (is = e, !0) : (is = null, !1)
    }
    var cd = typeof setTimeout == "function" ? setTimeout : void 0,
        e1 = typeof clearTimeout == "function" ? clearTimeout : void 0,
        sd = typeof Promise == "function" ? Promise : void 0,
        t1 = typeof queueMicrotask == "function" ? queueMicrotask : typeof sd < "u" ? function (e) {
            return sd.resolve(null).then(e).catch(l1)
        } : cd;

    function l1(e) {
        setTimeout(function () {
            throw e
        })
    }

    function El(e) {
        return e === "head"
    }

    function fd(e, t) {
        var l = t,
            a = 0;
        do {
            var n = l.nextSibling;
            if (e.removeChild(l), n && n.nodeType === 8)
                if (l = n.data, l === "/$" || l === "/&") {
                    if (a === 0) {
                        e.removeChild(n), _a(t);
                        return
                    }
                    a--
                } else if (l === "$" || l === "$?" || l === "$~" || l === "$!" || l === "&") a++;
            else if (l === "html") bn(e.ownerDocument.documentElement);
            else if (l === "head") {
                l = e.ownerDocument.head, bn(l);
                for (var u = l.firstChild; u;) {
                    var i = u.nextSibling,
                        s = u.nodeName;
                    u[Ba] || s === "SCRIPT" || s === "STYLE" || s === "LINK" && u.rel.toLowerCase() === "stylesheet" || l.removeChild(u), u = i
                }
            } else l === "body" && bn(e.ownerDocument.body);
            l = n
        } while (l);
        _a(t)
    }

    function od(e, t) {
        var l = e;
        e = 0;
        do {
            var a = l.nextSibling;
            if (l.nodeType === 1 ? t ? (l._stashedDisplay = l.style.display, l.style.display = "none") : (l.style.display = l._stashedDisplay || "", l.getAttribute("style") === "" && l.removeAttribute("style")) : l.nodeType === 3 && (t ? (l._stashedText = l.nodeValue, l.nodeValue = "") : l.nodeValue = l._stashedText || ""), a && a.nodeType === 8)
                if (l = a.data, l === "/$") {
                    if (e === 0) break;
                    e--
                } else l !== "$" && l !== "$?" && l !== "$~" && l !== "$!" || e++;
            l = a
        } while (l)
    }

    function cs(e) {
        var t = e.firstChild;
        for (t && t.nodeType === 10 && (t = t.nextSibling); t;) {
            var l = t;
            switch (t = t.nextSibling, l.nodeName) {
            case "HTML":
            case "HEAD":
            case "BODY":
                cs(l), di(l);
                continue;
            case "SCRIPT":
            case "STYLE":
                continue;
            case "LINK":
                if (l.rel.toLowerCase() === "stylesheet") continue
            }
            e.removeChild(l)
        }
    }

    function a1(e, t, l, a) {
        for (; e.nodeType === 1;) {
            var n = l;
            if (e.nodeName.toLowerCase() !== t.toLowerCase()) {
                if (!a && (e.nodeName !== "INPUT" || e.type !== "hidden")) break
            } else if (a) {
                if (!e[Ba]) switch (t) {
                case "meta":
                    if (!e.hasAttribute("itemprop")) break;
                    return e;
                case "link":
                    if (u = e.getAttribute("rel"), u === "stylesheet" && e.hasAttribute("data-precedence")) break;
                    if (u !== n.rel || e.getAttribute("href") !== (n.href == null || n.href === "" ? null : n.href) || e.getAttribute("crossorigin") !== (n.crossOrigin == null ? null : n.crossOrigin) || e.getAttribute("title") !== (n.title == null ? null : n.title)) break;
                    return e;
                case "style":
                    if (e.hasAttribute("data-precedence")) break;
                    return e;
                case "script":
                    if (u = e.getAttribute("src"), (u !== (n.src == null ? null : n.src) || e.getAttribute("type") !== (n.type == null ? null : n.type) || e.getAttribute("crossorigin") !== (n.crossOrigin == null ? null : n.crossOrigin)) && u && e.hasAttribute("async") && !e.hasAttribute("itemprop")) break;
                    return e;
                default:
                    return e
                }
            } else if (t === "input" && e.type === "hidden") {
                var u = n.name == null ? null : "" + n.name;
                if (n.type === "hidden" && e.getAttribute("name") === u) return e
            } else return e;
            if (e = At(e.nextSibling), e === null) break
        }
        return null
    }

    function n1(e, t, l) {
        if (t === "") return null;
        for (; e.nodeType !== 3;)
            if ((e.nodeType !== 1 || e.nodeName !== "INPUT" || e.type !== "hidden") && !l || (e = At(e.nextSibling), e === null)) return null;
        return e
    }

    function rd(e, t) {
        for (; e.nodeType !== 8;)
            if ((e.nodeType !== 1 || e.nodeName !== "INPUT" || e.type !== "hidden") && !t || (e = At(e.nextSibling), e === null)) return null;
        return e
    }

    function ss(e) {
        return e.data === "$?" || e.data === "$~"
    }

    function fs(e) {
        return e.data === "$!" || e.data === "$?" && e.ownerDocument.readyState !== "loading"
    }

    function u1(e, t) {
        var l = e.ownerDocument;
        if (e.data === "$~") e._reactRetry = t;
        else if (e.data !== "$?" || l.readyState !== "loading") t();
        else {
            var a = function () {
                t(), l.removeEventListener("DOMContentLoaded", a)
            };
            l.addEventListener("DOMContentLoaded", a), e._reactRetry = a
        }
    }

    function At(e) {
        for (; e != null; e = e.nextSibling) {
            var t = e.nodeType;
            if (t === 1 || t === 3) break;
            if (t === 8) {
                if (t = e.data, t === "$" || t === "$!" || t === "$?" || t === "$~" || t === "&" || t === "F!" || t === "F") break;
                if (t === "/$" || t === "/&") return null
            }
        }
        return e
    }
    var os = null;

    function dd(e) {
        e = e.nextSibling;
        for (var t = 0; e;) {
            if (e.nodeType === 8) {
                var l = e.data;
                if (l === "/$" || l === "/&") {
                    if (t === 0) return At(e.nextSibling);
                    t--
                } else l !== "$" && l !== "$!" && l !== "$?" && l !== "$~" && l !== "&" || t++
            }
            e = e.nextSibling
        }
        return null
    }

    function md(e) {
        e = e.previousSibling;
        for (var t = 0; e;) {
            if (e.nodeType === 8) {
                var l = e.data;
                if (l === "$" || l === "$!" || l === "$?" || l === "$~" || l === "&") {
                    if (t === 0) return e;
                    t--
                } else l !== "/$" && l !== "/&" || t++
            }
            e = e.previousSibling
        }
        return null
    }

    function hd(e, t, l) {
        switch (t = Hu(l), e) {
        case "html":
            if (e = t.documentElement, !e) throw Error(o(452));
            return e;
        case "head":
            if (e = t.head, !e) throw Error(o(453));
            return e;
        case "body":
            if (e = t.body, !e) throw Error(o(454));
            return e;
        default:
            throw Error(o(451))
        }
    }

    function bn(e) {
        for (var t = e.attributes; t.length;) e.removeAttributeNode(t[0]);
        di(e)
    }
    var _t = new Map,
        vd = new Set;

    function qu(e) {
        return typeof e.getRootNode == "function" ? e.getRootNode() : e.nodeType === 9 ? e : e.ownerDocument
    }
    var ll = H.d;
    H.d = {
        f: i1,
        r: c1,
        D: s1,
        C: f1,
        L: o1,
        m: r1,
        X: m1,
        S: d1,
        M: h1
    };

    function i1() {
        var e = ll.f(),
            t = Mu();
        return e || t
    }

    function c1(e) {
        var t = Wl(e);
        t !== null && t.tag === 5 && t.type === "form" ? Ro(t) : ll.r(e)
    }
    var Ma = typeof document > "u" ? null : document;

    function gd(e, t, l) {
        var a = Ma;
        if (a && typeof t == "string" && t) {
            var n = Et(t);
            n = 'link[rel="' + e + '"][href="' + n + '"]', typeof l == "string" && (n += '[crossorigin="' + l + '"]'), vd.has(n) || (vd.add(n), e = {
                rel: e,
                crossOrigin: l,
                href: t
            }, a.querySelector(n) === null && (t = a.createElement("link"), Fe(t, "link", e), Ve(t), a.head.appendChild(t)))
        }
    }

    function s1(e) {
        ll.D(e), gd("dns-prefetch", e, null)
    }

    function f1(e, t) {
        ll.C(e, t), gd("preconnect", e, t)
    }

    function o1(e, t, l) {
        ll.L(e, t, l);
        var a = Ma;
        if (a && e && t) {
            var n = 'link[rel="preload"][as="' + Et(t) + '"]';
            t === "image" && l && l.imageSrcSet ? (n += '[imagesrcset="' + Et(l.imageSrcSet) + '"]', typeof l.imageSizes == "string" && (n += '[imagesizes="' + Et(l.imageSizes) + '"]')) : n += '[href="' + Et(e) + '"]';
            var u = n;
            switch (t) {
            case "style":
                u = Da(e);
                break;
            case "script":
                u = Aa(e)
            }
            _t.has(u) || (e = M({
                rel: "preload",
                href: t === "image" && l && l.imageSrcSet ? void 0 : e,
                as: t
            }, l), _t.set(u, e), a.querySelector(n) !== null || t === "style" && a.querySelector(Nn(u)) || t === "script" && a.querySelector(En(u)) || (t = a.createElement("link"), Fe(t, "link", e), Ve(t), a.head.appendChild(t)))
        }
    }

    function r1(e, t) {
        ll.m(e, t);
        var l = Ma;
        if (l && e) {
            var a = t && typeof t.as == "string" ? t.as : "script",
                n = 'link[rel="modulepreload"][as="' + Et(a) + '"][href="' + Et(e) + '"]',
                u = n;
            switch (a) {
            case "audioworklet":
            case "paintworklet":
            case "serviceworker":
            case "sharedworker":
            case "worker":
            case "script":
                u = Aa(e)
            }
            if (!_t.has(u) && (e = M({
                    rel: "modulepreload",
                    href: e
                }, t), _t.set(u, e), l.querySelector(n) === null)) {
                switch (a) {
                case "audioworklet":
                case "paintworklet":
                case "serviceworker":
                case "sharedworker":
                case "worker":
                case "script":
                    if (l.querySelector(En(u))) return
                }
                a = l.createElement("link"), Fe(a, "link", e), Ve(a), l.head.appendChild(a)
            }
        }
    }

    function d1(e, t, l) {
        ll.S(e, t, l);
        var a = Ma;
        if (a && e) {
            var n = $l(a).hoistableStyles,
                u = Da(e);
            t = t || "default";
            var i = n.get(u);
            if (!i) {
                var s = {
                    loading: 0,
                    preload: null
                };
                if (i = a.querySelector(Nn(u))) s.loading = 5;
                else {
                    e = M({
                        rel: "stylesheet",
                        href: e,
                        "data-precedence": t
                    }, l), (l = _t.get(u)) && rs(e, l);
                    var r = i = a.createElement("link");
                    Ve(r), Fe(r, "link", e), r._p = new Promise(function (y, T) {
                        r.onload = y, r.onerror = T
                    }), r.addEventListener("load", function () {
                        s.loading |= 1
                    }), r.addEventListener("error", function () {
                        s.loading |= 2
                    }), s.loading |= 4, Bu(i, t, a)
                }
                i = {
                    type: "stylesheet",
                    instance: i,
                    count: 1,
                    state: s
                }, n.set(u, i)
            }
        }
    }

    function m1(e, t) {
        ll.X(e, t);
        var l = Ma;
        if (l && e) {
            var a = $l(l).hoistableScripts,
                n = Aa(e),
                u = a.get(n);
            u || (u = l.querySelector(En(n)), u || (e = M({
                src: e,
                async: !0
            }, t), (t = _t.get(n)) && ds(e, t), u = l.createElement("script"), Ve(u), Fe(u, "link", e), l.head.appendChild(u)), u = {
                type: "script",
                instance: u,
                count: 1,
                state: null
            }, a.set(n, u))
        }
    }

    function h1(e, t) {
        ll.M(e, t);
        var l = Ma;
        if (l && e) {
            var a = $l(l).hoistableScripts,
                n = Aa(e),
                u = a.get(n);
            u || (u = l.querySelector(En(n)), u || (e = M({
                src: e,
                async: !0,
                type: "module"
            }, t), (t = _t.get(n)) && ds(e, t), u = l.createElement("script"), Ve(u), Fe(u, "link", e), l.head.appendChild(u)), u = {
                type: "script",
                instance: u,
                count: 1,
                state: null
            }, a.set(n, u))
        }
    }

    function yd(e, t, l, a) {
        var n = (n = ue.current) ? qu(n) : null;
        if (!n) throw Error(o(446));
        switch (e) {
        case "meta":
        case "title":
            return null;
        case "style":
            return typeof l.precedence == "string" && typeof l.href == "string" ? (t = Da(l.href), l = $l(n).hoistableStyles, a = l.get(t), a || (a = {
                type: "style",
                instance: null,
                count: 0,
                state: null
            }, l.set(t, a)), a) : {
                type: "void",
                instance: null,
                count: 0,
                state: null
            };
        case "link":
            if (l.rel === "stylesheet" && typeof l.href == "string" && typeof l.precedence == "string") {
                e = Da(l.href);
                var u = $l(n).hoistableStyles,
                    i = u.get(e);
                if (i || (n = n.ownerDocument || n, i = {
                        type: "stylesheet",
                        instance: null,
                        count: 0,
                        state: {
                            loading: 0,
                            preload: null
                        }
                    }, u.set(e, i), (u = n.querySelector(Nn(e))) && !u._p && (i.instance = u, i.state.loading = 5), _t.has(e) || (l = {
                        rel: "preload",
                        as: "style",
                        href: l.href,
                        crossOrigin: l.crossOrigin,
                        integrity: l.integrity,
                        media: l.media,
                        hrefLang: l.hrefLang,
                        referrerPolicy: l.referrerPolicy
                    }, _t.set(e, l), u || v1(n, e, l, i.state))), t && a === null) throw Error(o(528, ""));
                return i
            }
            if (t && a !== null) throw Error(o(529, ""));
            return null;
        case "script":
            return t = l.async, l = l.src, typeof l == "string" && t && typeof t != "function" && typeof t != "symbol" ? (t = Aa(l), l = $l(n).hoistableScripts, a = l.get(t), a || (a = {
                type: "script",
                instance: null,
                count: 0,
                state: null
            }, l.set(t, a)), a) : {
                type: "void",
                instance: null,
                count: 0,
                state: null
            };
        default:
            throw Error(o(444, e))
        }
    }

    function Da(e) {
        return 'href="' + Et(e) + '"'
    }

    function Nn(e) {
        return 'link[rel="stylesheet"][' + e + "]"
    }

    function pd(e) {
        return M({}, e, {
            "data-precedence": e.precedence,
            precedence: null
        })
    }

    function v1(e, t, l, a) {
        e.querySelector('link[rel="preload"][as="style"][' + t + "]") ? a.loading = 1 : (t = e.createElement("link"), a.preload = t, t.addEventListener("load", function () {
            return a.loading |= 1
        }), t.addEventListener("error", function () {
            return a.loading |= 2
        }), Fe(t, "link", l), Ve(t), e.head.appendChild(t))
    }

    function Aa(e) {
        return '[src="' + Et(e) + '"]'
    }

    function En(e) {
        return "script[async]" + e
    }

    function Sd(e, t, l) {
        if (t.count++, t.instance === null) switch (t.type) {
        case "style":
            var a = e.querySelector('style[data-href~="' + Et(l.href) + '"]');
            if (a) return t.instance = a, Ve(a), a;
            var n = M({}, l, {
                "data-href": l.href,
                "data-precedence": l.precedence,
                href: null,
                precedence: null
            });
            return a = (e.ownerDocument || e).createElement("style"), Ve(a), Fe(a, "style", n), Bu(a, l.precedence, e), t.instance = a;
        case "stylesheet":
            n = Da(l.href);
            var u = e.querySelector(Nn(n));
            if (u) return t.state.loading |= 4, t.instance = u, Ve(u), u;
            a = pd(l), (n = _t.get(n)) && rs(a, n), u = (e.ownerDocument || e).createElement("link"), Ve(u);
            var i = u;
            return i._p = new Promise(function (s, r) {
                i.onload = s, i.onerror = r
            }), Fe(u, "link", a), t.state.loading |= 4, Bu(u, l.precedence, e), t.instance = u;
        case "script":
            return u = Aa(l.src), (n = e.querySelector(En(u))) ? (t.instance = n, Ve(n), n) : (a = l, (n = _t.get(u)) && (a = M({}, l), ds(a, n)), e = e.ownerDocument || e, n = e.createElement("script"), Ve(n), Fe(n, "link", a), e.head.appendChild(n), t.instance = n);
        case "void":
            return null;
        default:
            throw Error(o(443, t.type))
        } else t.type === "stylesheet" && (t.state.loading & 4) === 0 && (a = t.instance, t.state.loading |= 4, Bu(a, l.precedence, e));
        return t.instance
    }

    function Bu(e, t, l) {
        for (var a = l.querySelectorAll('link[rel="stylesheet"][data-precedence],style[data-precedence]'), n = a.length ? a[a.length - 1] : null, u = n, i = 0; i < a.length; i++) {
            var s = a[i];
            if (s.dataset.precedence === t) u = s;
            else if (u !== n) break
        }
        u ? u.parentNode.insertBefore(e, u.nextSibling) : (t = l.nodeType === 9 ? l.head : l, t.insertBefore(e, t.firstChild))
    }

    function rs(e, t) {
        e.crossOrigin == null && (e.crossOrigin = t.crossOrigin), e.referrerPolicy == null && (e.referrerPolicy = t.referrerPolicy), e.title == null && (e.title = t.title)
    }

    function ds(e, t) {
        e.crossOrigin == null && (e.crossOrigin = t.crossOrigin), e.referrerPolicy == null && (e.referrerPolicy = t.referrerPolicy), e.integrity == null && (e.integrity = t.integrity)
    }
    var Lu = null;

    function bd(e, t, l) {
        if (Lu === null) {
            var a = new Map,
                n = Lu = new Map;
            n.set(l, a)
        } else n = Lu, a = n.get(l), a || (a = new Map, n.set(l, a));
        if (a.has(e)) return a;
        for (a.set(e, null), l = l.getElementsByTagName(e), n = 0; n < l.length; n++) {
            var u = l[n];
            if (!(u[Ba] || u[Ke] || e === "link" && u.getAttribute("rel") === "stylesheet") && u.namespaceURI !== "http://www.w3.org/2000/svg") {
                var i = u.getAttribute(t) || "";
                i = e + i;
                var s = a.get(i);
                s ? s.push(u) : a.set(i, [u])
            }
        }
        return a
    }

    function Nd(e, t, l) {
        e = e.ownerDocument || e, e.head.insertBefore(l, t === "title" ? e.querySelector("head > title") : null)
    }

    function g1(e, t, l) {
        if (l === 1 || t.itemProp != null) return !1;
        switch (e) {
        case "meta":
        case "title":
            return !0;
        case "style":
            if (typeof t.precedence != "string" || typeof t.href != "string" || t.href === "") break;
            return !0;
        case "link":
            if (typeof t.rel != "string" || typeof t.href != "string" || t.href === "" || t.onLoad || t.onError) break;
            return t.rel === "stylesheet" ? (e = t.disabled, typeof t.precedence == "string" && e == null) : !0;
        case "script":
            if (t.async && typeof t.async != "function" && typeof t.async != "symbol" && !t.onLoad && !t.onError && t.src && typeof t.src == "string") return !0
        }
        return !1
    }

    function Ed(e) {
        return !(e.type === "stylesheet" && (e.state.loading & 3) === 0)
    }

    function y1(e, t, l, a) {
        if (l.type === "stylesheet" && (typeof a.media != "string" || matchMedia(a.media).matches !== !1) && (l.state.loading & 4) === 0) {
            if (l.instance === null) {
                var n = Da(a.href),
                    u = t.querySelector(Nn(n));
                if (u) {
                    t = u._p, t !== null && typeof t == "object" && typeof t.then == "function" && (e.count++, e = ku.bind(e), t.then(e, e)), l.state.loading |= 4, l.instance = u, Ve(u);
                    return
                }
                u = t.ownerDocument || t, a = pd(a), (n = _t.get(n)) && rs(a, n), u = u.createElement("link"), Ve(u);
                var i = u;
                i._p = new Promise(function (s, r) {
                    i.onload = s, i.onerror = r
                }), Fe(u, "link", a), l.instance = u
            }
            e.stylesheets === null && (e.stylesheets = new Map), e.stylesheets.set(l, t), (t = l.state.preload) && (l.state.loading & 3) === 0 && (e.count++, l = ku.bind(e), t.addEventListener("load", l), t.addEventListener("error", l))
        }
    }
    var ms = 0;

    function p1(e, t) {
        return e.stylesheets && e.count === 0 && Gu(e, e.stylesheets), 0 < e.count || 0 < e.imgCount ? function (l) {
            var a = setTimeout(function () {
                if (e.stylesheets && Gu(e, e.stylesheets), e.unsuspend) {
                    var u = e.unsuspend;
                    e.unsuspend = null, u()
                }
            }, 6e4 + t);
            0 < e.imgBytes && ms === 0 && (ms = 62500 * Ih());
            var n = setTimeout(function () {
                if (e.waitingForImages = !1, e.count === 0 && (e.stylesheets && Gu(e, e.stylesheets), e.unsuspend)) {
                    var u = e.unsuspend;
                    e.unsuspend = null, u()
                }
            }, (e.imgBytes > ms ? 50 : 800) + t);
            return e.unsuspend = l,
                function () {
                    e.unsuspend = null, clearTimeout(a), clearTimeout(n)
                }
        } : null
    }

    function ku() {
        if (this.count--, this.count === 0 && (this.imgCount === 0 || !this.waitingForImages)) {
            if (this.stylesheets) Gu(this, this.stylesheets);
            else if (this.unsuspend) {
                var e = this.unsuspend;
                this.unsuspend = null, e()
            }
        }
    }
    var Yu = null;

    function Gu(e, t) {
        e.stylesheets = null, e.unsuspend !== null && (e.count++, Yu = new Map, t.forEach(S1, e), Yu = null, ku.call(e))
    }

    function S1(e, t) {
        if (!(t.state.loading & 4)) {
            var l = Yu.get(e);
            if (l) var a = l.get(null);
            else {
                l = new Map, Yu.set(e, l);
                for (var n = e.querySelectorAll("link[data-precedence],style[data-precedence]"), u = 0; u < n.length; u++) {
                    var i = n[u];
                    (i.nodeName === "LINK" || i.getAttribute("media") !== "not all") && (l.set(i.dataset.precedence, i), a = i)
                }
                a && l.set(null, a)
            }
            n = t.instance, i = n.getAttribute("data-precedence"), u = l.get(i) || a, u === a && l.set(null, n), l.set(i, n), this.count++, a = ku.bind(this), n.addEventListener("load", a), n.addEventListener("error", a), u ? u.parentNode.insertBefore(n, u.nextSibling) : (e = e.nodeType === 9 ? e.head : e, e.insertBefore(n, e.firstChild)), t.state.loading |= 4
        }
    }
    var Tn = {
        $$typeof: F,
        Provider: null,
        Consumer: null,
        _currentValue: I,
        _currentValue2: I,
        _threadCount: 0
    };

    function b1(e, t, l, a, n, u, i, s, r) {
        this.tag = 1, this.containerInfo = e, this.pingCache = this.current = this.pendingChildren = null, this.timeoutHandle = -1, this.callbackNode = this.next = this.pendingContext = this.context = this.cancelPendingCommit = null, this.callbackPriority = 0, this.expirationTimes = si(-1), this.entangledLanes = this.shellSuspendCounter = this.errorRecoveryDisabledLanes = this.expiredLanes = this.warmLanes = this.pingedLanes = this.suspendedLanes = this.pendingLanes = 0, this.entanglements = si(0), this.hiddenUpdates = si(null), this.identifierPrefix = a, this.onUncaughtError = n, this.onCaughtError = u, this.onRecoverableError = i, this.pooledCache = null, this.pooledCacheLanes = 0, this.formState = r, this.incompleteTransitions = new Map
    }

    function Td(e, t, l, a, n, u, i, s, r, y, T, D) {
        return e = new b1(e, t, l, i, r, y, T, D, s), t = 1, u === !0 && (t |= 24), u = vt(3, null, null, t), e.current = u, u.stateNode = e, t = Zi(), t.refCount++, e.pooledCache = t, t.refCount++, u.memoizedState = {
            element: a,
            isDehydrated: l,
            cache: t
        }, $i(u), e
    }

    function xd(e) {
        return e ? (e = ia, e) : ia
    }

    function zd(e, t, l, a, n, u) {
        n = xd(n), a.context === null ? a.context = n : a.pendingContext = n, a = rl(t), a.payload = {
            element: l
        }, u = u === void 0 ? null : u, u !== null && (a.callback = u), l = dl(e, a, t), l !== null && (ft(l, e, t), en(l, e, t))
    }

    function jd(e, t) {
        if (e = e.memoizedState, e !== null && e.dehydrated !== null) {
            var l = e.retryLane;
            e.retryLane = l !== 0 && l < t ? l : t
        }
    }

    function hs(e, t) {
        jd(e, t), (e = e.alternate) && jd(e, t)
    }

    function Md(e) {
        if (e.tag === 13 || e.tag === 31) {
            var t = Cl(e, 67108864);
            t !== null && ft(t, e, 67108864), hs(e, 67108864)
        }
    }

    function Dd(e) {
        if (e.tag === 13 || e.tag === 31) {
            var t = bt();
            t = fi(t);
            var l = Cl(e, t);
            l !== null && ft(l, e, t), hs(e, t)
        }
    }
    var Xu = !0;

    function N1(e, t, l, a) {
        var n = x.T;
        x.T = null;
        var u = H.p;
        try {
            H.p = 2, vs(e, t, l, a)
        } finally {
            H.p = u, x.T = n
        }
    }

    function E1(e, t, l, a) {
        var n = x.T;
        x.T = null;
        var u = H.p;
        try {
            H.p = 8, vs(e, t, l, a)
        } finally {
            H.p = u, x.T = n
        }
    }

    function vs(e, t, l, a) {
        if (Xu) {
            var n = gs(a);
            if (n === null) ts(e, t, a, Qu, l), _d(e, a);
            else if (x1(n, e, t, l, a)) a.stopPropagation();
            else if (_d(e, a), t & 4 && -1 < T1.indexOf(e)) {
                for (; n !== null;) {
                    var u = Wl(n);
                    if (u !== null) switch (u.tag) {
                    case 3:
                        if (u = u.stateNode, u.current.memoizedState.isDehydrated) {
                            var i = Al(u.pendingLanes);
                            if (i !== 0) {
                                var s = u;
                                for (s.pendingLanes |= 2, s.entangledLanes |= 2; i;) {
                                    var r = 1 << 31 - mt(i);
                                    s.entanglements[1] |= r, i &= ~r
                                }
                                Lt(u), (he & 6) === 0 && (zu = rt() + 500, yn(0))
                            }
                        }
                        break;
                    case 31:
                    case 13:
                        s = Cl(u, 2), s !== null && ft(s, u, 2), Mu(), hs(u, 2)
                    }
                    if (u = gs(a), u === null && ts(e, t, a, Qu, l), u === n) break;
                    n = u
                }
                n !== null && a.stopPropagation()
            } else ts(e, t, a, null, l)
        }
    }

    function gs(e) {
        return e = pi(e), ys(e)
    }
    var Qu = null;

    function ys(e) {
        if (Qu = null, e = Jl(e), e !== null) {
            var t = z(e);
            if (t === null) e = null;
            else {
                var l = t.tag;
                if (l === 13) {
                    if (e = C(t), e !== null) return e;
                    e = null
                } else if (l === 31) {
                    if (e = R(t), e !== null) return e;
                    e = null
                } else if (l === 3) {
                    if (t.stateNode.current.memoizedState.isDehydrated) return t.tag === 3 ? t.stateNode.containerInfo : null;
                    e = null
                } else t !== e && (e = null)
            }
        }
        return Qu = e, null
    }

    function Ad(e) {
        switch (e) {
        case "beforetoggle":
        case "cancel":
        case "click":
        case "close":
        case "contextmenu":
        case "copy":
        case "cut":
        case "auxclick":
        case "dblclick":
        case "dragend":
        case "dragstart":
        case "drop":
        case "focusin":
        case "focusout":
        case "input":
        case "invalid":
        case "keydown":
        case "keypress":
        case "keyup":
        case "mousedown":
        case "mouseup":
        case "paste":
        case "pause":
        case "play":
        case "pointercancel":
        case "pointerdown":
        case "pointerup":
        case "ratechange":
        case "reset":
        case "resize":
        case "seeked":
        case "submit":
        case "toggle":
        case "touchcancel":
        case "touchend":
        case "touchstart":
        case "volumechange":
        case "change":
        case "selectionchange":
        case "textInput":
        case "compositionstart":
        case "compositionend":
        case "compositionupdate":
        case "beforeblur":
        case "afterblur":
        case "beforeinput":
        case "blur":
        case "fullscreenchange":
        case "focus":
        case "hashchange":
        case "popstate":
        case "select":
        case "selectstart":
            return 2;
        case "drag":
        case "dragenter":
        case "dragexit":
        case "dragleave":
        case "dragover":
        case "mousemove":
        case "mouseout":
        case "mouseover":
        case "pointermove":
        case "pointerout":
        case "pointerover":
        case "scroll":
        case "touchmove":
        case "wheel":
        case "mouseenter":
        case "mouseleave":
        case "pointerenter":
        case "pointerleave":
            return 8;
        case "message":
            switch (sm()) {
            case Hs:
                return 2;
            case qs:
                return 8;
            case Rn:
            case fm:
                return 32;
            case Bs:
                return 268435456;
            default:
                return 32
            }
            default:
                return 32
        }
    }
    var ps = !1,
        Tl = null,
        xl = null,
        zl = null,
        xn = new Map,
        zn = new Map,
        jl = [],
        T1 = "mousedown mouseup touchcancel touchend touchstart auxclick dblclick pointercancel pointerdown pointerup dragend dragstart drop compositionend compositionstart keydown keypress keyup input textInput copy cut paste click change contextmenu reset".split(" ");

    function _d(e, t) {
        switch (e) {
        case "focusin":
        case "focusout":
            Tl = null;
            break;
        case "dragenter":
        case "dragleave":
            xl = null;
            break;
        case "mouseover":
        case "mouseout":
            zl = null;
            break;
        case "pointerover":
        case "pointerout":
            xn.delete(t.pointerId);
            break;
        case "gotpointercapture":
        case "lostpointercapture":
            zn.delete(t.pointerId)
        }
    }

    function jn(e, t, l, a, n, u) {
        return e === null || e.nativeEvent !== u ? (e = {
            blockedOn: t,
            domEventName: l,
            eventSystemFlags: a,
            nativeEvent: u,
            targetContainers: [n]
        }, t !== null && (t = Wl(t), t !== null && Md(t)), e) : (e.eventSystemFlags |= a, t = e.targetContainers, n !== null && t.indexOf(n) === -1 && t.push(n), e)
    }

    function x1(e, t, l, a, n) {
        switch (t) {
        case "focusin":
            return Tl = jn(Tl, e, t, l, a, n), !0;
        case "dragenter":
            return xl = jn(xl, e, t, l, a, n), !0;
        case "mouseover":
            return zl = jn(zl, e, t, l, a, n), !0;
        case "pointerover":
            var u = n.pointerId;
            return xn.set(u, jn(xn.get(u) || null, e, t, l, a, n)), !0;
        case "gotpointercapture":
            return u = n.pointerId, zn.set(u, jn(zn.get(u) || null, e, t, l, a, n)), !0
        }
        return !1
    }

    function Od(e) {
        var t = Jl(e.target);
        if (t !== null) {
            var l = z(t);
            if (l !== null) {
                if (t = l.tag, t === 13) {
                    if (t = C(l), t !== null) {
                        e.blockedOn = t, Qs(e.priority, function () {
                            Dd(l)
                        });
                        return
                    }
                } else if (t === 31) {
                    if (t = R(l), t !== null) {
                        e.blockedOn = t, Qs(e.priority, function () {
                            Dd(l)
                        });
                        return
                    }
                } else if (t === 3 && l.stateNode.current.memoizedState.isDehydrated) {
                    e.blockedOn = l.tag === 3 ? l.stateNode.containerInfo : null;
                    return
                }
            }
        }
        e.blockedOn = null
    }

    function Vu(e) {
        if (e.blockedOn !== null) return !1;
        for (var t = e.targetContainers; 0 < t.length;) {
            var l = gs(e.nativeEvent);
            if (l === null) {
                l = e.nativeEvent;
                var a = new l.constructor(l.type, l);
                yi = a, l.target.dispatchEvent(a), yi = null
            } else return t = Wl(l), t !== null && Md(t), e.blockedOn = l, !1;
            t.shift()
        }
        return !0
    }

    function Rd(e, t, l) {
        Vu(e) && l.delete(t)
    }

    function z1() {
        ps = !1, Tl !== null && Vu(Tl) && (Tl = null), xl !== null && Vu(xl) && (xl = null), zl !== null && Vu(zl) && (zl = null), xn.forEach(Rd), zn.forEach(Rd)
    }

    function wu(e, t) {
        e.blockedOn === t && (e.blockedOn = null, ps || (ps = !0, f.unstable_scheduleCallback(f.unstable_NormalPriority, z1)))
    }
    var Zu = null;

    function Ud(e) {
        Zu !== e && (Zu = e, f.unstable_scheduleCallback(f.unstable_NormalPriority, function () {
            Zu === e && (Zu = null);
            for (var t = 0; t < e.length; t += 3) {
                var l = e[t],
                    a = e[t + 1],
                    n = e[t + 2];
                if (typeof a != "function") {
                    if (ys(a || l) === null) continue;
                    break
                }
                var u = Wl(l);
                u !== null && (e.splice(t, 3), t -= 3, gc(u, {
                    pending: !0,
                    data: n,
                    method: l.method,
                    action: a
                }, a, n))
            }
        }))
    }

    function _a(e) {
        function t(r) {
            return wu(r, e)
        }
        Tl !== null && wu(Tl, e), xl !== null && wu(xl, e), zl !== null && wu(zl, e), xn.forEach(t), zn.forEach(t);
        for (var l = 0; l < jl.length; l++) {
            var a = jl[l];
            a.blockedOn === e && (a.blockedOn = null)
        }
        for (; 0 < jl.length && (l = jl[0], l.blockedOn === null);) Od(l), l.blockedOn === null && jl.shift();
        if (l = (e.ownerDocument || e).$$reactFormReplay, l != null)
            for (a = 0; a < l.length; a += 3) {
                var n = l[a],
                    u = l[a + 1],
                    i = n[at] || null;
                if (typeof u == "function") i || Ud(l);
                else if (i) {
                    var s = null;
                    if (u && u.hasAttribute("formAction")) {
                        if (n = u, i = u[at] || null) s = i.formAction;
                        else if (ys(n) !== null) continue
                    } else s = i.action;
                    typeof s == "function" ? l[a + 1] = s : (l.splice(a, 3), a -= 3), Ud(l)
                }
            }
    }

    function Cd() {
        function e(u) {
            u.canIntercept && u.info === "react-transition" && u.intercept({
                handler: function () {
                    return new Promise(function (i) {
                        return n = i
                    })
                },
                focusReset: "manual",
                scroll: "manual"
            })
        }

        function t() {
            n !== null && (n(), n = null), a || setTimeout(l, 20)
        }

        function l() {
            if (!a && !navigation.transition) {
                var u = navigation.currentEntry;
                u && u.url != null && navigation.navigate(u.url, {
                    state: u.getState(),
                    info: "react-transition",
                    history: "replace"
                })
            }
        }
        if (typeof navigation == "object") {
            var a = !1,
                n = null;
            return navigation.addEventListener("navigate", e), navigation.addEventListener("navigatesuccess", t), navigation.addEventListener("navigateerror", t), setTimeout(l, 100),
                function () {
                    a = !0, navigation.removeEventListener("navigate", e), navigation.removeEventListener("navigatesuccess", t), navigation.removeEventListener("navigateerror", t), n !== null && (n(), n = null)
                }
        }
    }

    function Ss(e) {
        this._internalRoot = e
    }
    Ku.prototype.render = Ss.prototype.render = function (e) {
        var t = this._internalRoot;
        if (t === null) throw Error(o(409));
        var l = t.current,
            a = bt();
        zd(l, a, e, t, null, null)
    }, Ku.prototype.unmount = Ss.prototype.unmount = function () {
        var e = this._internalRoot;
        if (e !== null) {
            this._internalRoot = null;
            var t = e.containerInfo;
            zd(e.current, 2, null, e, null, null), Mu(), t[Kl] = null
        }
    };

    function Ku(e) {
        this._internalRoot = e
    }
    Ku.prototype.unstable_scheduleHydration = function (e) {
        if (e) {
            var t = Xs();
            e = {
                blockedOn: null,
                target: e,
                priority: t
            };
            for (var l = 0; l < jl.length && t !== 0 && t < jl[l].priority; l++);
            jl.splice(l, 0, e), l === 0 && Od(e)
        }
    };
    var Hd = b.version;
    if (Hd !== "19.2.3") throw Error(o(527, Hd, "19.2.3"));
    H.findDOMNode = function (e) {
        var t = e._reactInternals;
        if (t === void 0) throw typeof e.render == "function" ? Error(o(188)) : (e = Object.keys(e).join(","), Error(o(268, e)));
        return e = S(t), e = e !== null ? q(e) : null, e = e === null ? null : e.stateNode, e
    };
    var j1 = {
        bundleType: 0,
        version: "19.2.3",
        rendererPackageName: "react-dom",
        currentDispatcherRef: x,
        reconcilerVersion: "19.2.3"
    };
    if (typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ < "u") {
        var Ju = __REACT_DEVTOOLS_GLOBAL_HOOK__;
        if (!Ju.isDisabled && Ju.supportsFiber) try {
            Ca = Ju.inject(j1), dt = Ju
        } catch {}
    }
    return Dn.createRoot = function (e, t) {
        if (!h(e)) throw Error(o(299));
        var l = !1,
            a = "",
            n = Xo,
            u = Qo,
            i = Vo;
        return t != null && (t.unstable_strictMode === !0 && (l = !0), t.identifierPrefix !== void 0 && (a = t.identifierPrefix), t.onUncaughtError !== void 0 && (n = t.onUncaughtError), t.onCaughtError !== void 0 && (u = t.onCaughtError), t.onRecoverableError !== void 0 && (i = t.onRecoverableError)), t = Td(e, 1, !1, null, null, l, a, null, n, u, i, Cd), e[Kl] = t.current, es(e), new Ss(t)
    }, Dn.hydrateRoot = function (e, t, l) {
        if (!h(e)) throw Error(o(299));
        var a = !1,
            n = "",
            u = Xo,
            i = Qo,
            s = Vo,
            r = null;
        return l != null && (l.unstable_strictMode === !0 && (a = !0), l.identifierPrefix !== void 0 && (n = l.identifierPrefix), l.onUncaughtError !== void 0 && (u = l.onUncaughtError), l.onCaughtError !== void 0 && (i = l.onCaughtError), l.onRecoverableError !== void 0 && (s = l.onRecoverableError), l.formState !== void 0 && (r = l.formState)), t = Td(e, 1, !0, t, l ?? null, a, n, r, u, i, s, Cd), t.context = xd(null), l = t.current, a = bt(), a = fi(a), n = rl(a), n.callback = null, dl(l, n, a), l = a, t.current.lanes = l, qa(t, l), Lt(t), e[Kl] = t.current, es(e), new Ku(t)
    }, Dn.version = "19.2.3", Dn
}
var wd;

function B1() {
    if (wd) return Es.exports;
    wd = 1;

    function f() {
        if (!(typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ > "u" || typeof __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE != "function")) try {
            __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE(f)
        } catch (b) {
            console.error(b)
        }
    }
    return f(), Es.exports = q1(), Es.exports
}
var L1 = B1();
const k1 = f => f.replace(/([a-z0-9])([A-Z])/g, "$1-$2").toLowerCase(),
    Y1 = f => f.replace(/^([A-Z])|[\s-_]+(\w)/g, (b, N, o) => o ? o.toUpperCase() : N.toLowerCase()),
    Zd = f => {
        const b = Y1(f);
        return b.charAt(0).toUpperCase() + b.slice(1)
    },
    Fd = (...f) => f.filter((b, N, o) => !!b && b.trim() !== "" && o.indexOf(b) === N).join(" ").trim(),
    G1 = f => {
        for (const b in f)
            if (b.startsWith("aria-") || b === "role" || b === "title") return !0
    };
var X1 = {
    xmlns: "http://www.w3.org/2000/svg",
    width: 24,
    height: 24,
    viewBox: "0 0 24 24",
    fill: "none",
    stroke: "currentColor",
    strokeWidth: 2,
    strokeLinecap: "round",
    strokeLinejoin: "round"
};
const Q1 = L.forwardRef(({
    color: f = "currentColor",
    size: b = 24,
    strokeWidth: N = 2,
    absoluteStrokeWidth: o,
    className: h = "",
    children: z,
    iconNode: C,
    ...R
}, _) => L.createElement("svg", {
    ref: _,
    ...X1,
    width: b,
    height: b,
    stroke: f,
    strokeWidth: o ? Number(N) * 24 / Number(b) : N,
    className: Fd("lucide", h),
    ...!z && !G1(R) && {
        "aria-hidden": "true"
    },
    ...R
}, [...C.map(([S, q]) => L.createElement(S, q)), ...Array.isArray(z) ? z : [z]]));
const se = (f, b) => {
    const N = L.forwardRef(({
        className: o,
        ...h
    }, z) => L.createElement(Q1, {
        ref: z,
        iconNode: b,
        className: Fd(`lucide-${k1(Zd(f))}`, `lucide-${f}`, o),
        ...h
    }));
    return N.displayName = Zd(f), N
};
const V1 = [
        ["path", {
            d: "M10.268 21a2 2 0 0 0 3.464 0",
            key: "vwvbt9"
        }],
        ["path", {
            d: "M3.262 15.326A1 1 0 0 0 4 17h16a1 1 0 0 0 .74-1.673C19.41 13.956 18 12.499 18 8A6 6 0 0 0 6 8c0 4.499-1.411 5.956-2.738 7.326",
            key: "11g9vi"
        }]
    ],
    w1 = se("bell", V1);
const Z1 = [
        ["path", {
            d: "M3 3v16a2 2 0 0 0 2 2h16",
            key: "c24i48"
        }],
        ["path", {
            d: "M18 17V9",
            key: "2bz60n"
        }],
        ["path", {
            d: "M13 17V5",
            key: "1frdt8"
        }],
        ["path", {
            d: "M8 17v-3",
            key: "17ska0"
        }]
    ],
    Id = se("chart-column", Z1);
const K1 = [
        ["path", {
            d: "m6 9 6 6 6-6",
            key: "qrunsl"
        }]
    ],
    Iu = se("chevron-down", K1);
const J1 = [
        ["circle", {
            cx: "12",
            cy: "12",
            r: "10",
            key: "1mglay"
        }],
        ["line", {
            x1: "12",
            x2: "12",
            y1: "8",
            y2: "12",
            key: "1pkeuh"
        }],
        ["line", {
            x1: "12",
            x2: "12.01",
            y1: "16",
            y2: "16",
            key: "4dfq90"
        }]
    ],
    Pd = se("circle-alert", J1);
const W1 = [
        ["path", {
            d: "M21.801 10A10 10 0 1 1 17 3.335",
            key: "yps3ct"
        }],
        ["path", {
            d: "m9 11 3 3L22 4",
            key: "1pflzl"
        }]
    ],
    js = se("circle-check-big", W1);
const $1 = [
        ["path", {
            d: "M11.562 3.266a.5.5 0 0 1 .876 0L15.39 8.87a1 1 0 0 0 1.516.294L21.183 5.5a.5.5 0 0 1 .798.519l-2.834 10.246a1 1 0 0 1-.956.734H5.81a1 1 0 0 1-.957-.734L2.02 6.02a.5.5 0 0 1 .798-.519l4.276 3.664a1 1 0 0 0 1.516-.294z",
            key: "1vdc57"
        }],
        ["path", {
            d: "M5 21h14",
            key: "11awu3"
        }]
    ],
    ti = se("crown", $1);
const F1 = [
        ["path", {
            d: "M12 15V3",
            key: "m9g1x1"
        }],
        ["path", {
            d: "M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4",
            key: "ih7n3h"
        }],
        ["path", {
            d: "m7 10 5 5 5-5",
            key: "brsn70"
        }]
    ],
    I1 = se("download", F1);
const P1 = [
        ["path", {
            d: "M15 3h6v6",
            key: "1q9fwt"
        }],
        ["path", {
            d: "M10 14 21 3",
            key: "gplh6r"
        }],
        ["path", {
            d: "M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6",
            key: "a6xqqp"
        }]
    ],
    Os = se("external-link", P1);
const e0 = [
        ["rect", {
            width: "18",
            height: "18",
            x: "3",
            y: "3",
            rx: "2",
            key: "afitv7"
        }],
        ["path", {
            d: "M7 3v18",
            key: "bbkbws"
        }],
        ["path", {
            d: "M3 7.5h4",
            key: "zfgn84"
        }],
        ["path", {
            d: "M3 12h18",
            key: "1i2n21"
        }],
        ["path", {
            d: "M3 16.5h4",
            key: "1230mu"
        }],
        ["path", {
            d: "M17 3v18",
            key: "in4fa5"
        }],
        ["path", {
            d: "M17 7.5h4",
            key: "myr1c1"
        }],
        ["path", {
            d: "M17 16.5h4",
            key: "go4c1d"
        }]
    ],
    t0 = se("film", e0);
const l0 = [
        ["path", {
            d: "M15 21v-8a1 1 0 0 0-1-1h-4a1 1 0 0 0-1 1v8",
            key: "5wwlr5"
        }],
        ["path", {
            d: "M3 10a2 2 0 0 1 .709-1.528l7-6a2 2 0 0 1 2.582 0l7 6A2 2 0 0 1 21 10v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z",
            key: "r6nss1"
        }]
    ],
    a0 = se("house", l0);
const n0 = [
        ["path", {
            d: "M12 2v4",
            key: "3427ic"
        }],
        ["path", {
            d: "m16.2 7.8 2.9-2.9",
            key: "r700ao"
        }],
        ["path", {
            d: "M18 12h4",
            key: "wj9ykh"
        }],
        ["path", {
            d: "m16.2 16.2 2.9 2.9",
            key: "1bxg5t"
        }],
        ["path", {
            d: "M12 18v4",
            key: "jadmvz"
        }],
        ["path", {
            d: "m4.9 19.1 2.9-2.9",
            key: "bwix9q"
        }],
        ["path", {
            d: "M2 12h4",
            key: "j09sii"
        }],
        ["path", {
            d: "m4.9 4.9 2.9 2.9",
            key: "giyufr"
        }]
    ],
    Pu = se("loader", n0);
const u0 = [
        ["rect", {
            width: "18",
            height: "11",
            x: "3",
            y: "11",
            rx: "2",
            ry: "2",
            key: "1w4ew1"
        }],
        ["path", {
            d: "M7 11V7a5 5 0 0 1 10 0v4",
            key: "fwvmzm"
        }]
    ],
    Ct = se("lock", u0);
const i0 = [
        ["path", {
            d: "m10 17 5-5-5-5",
            key: "1bsop3"
        }],
        ["path", {
            d: "M15 12H3",
            key: "6jk70r"
        }],
        ["path", {
            d: "M15 3h4a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2h-4",
            key: "u53s6r"
        }]
    ],
    c0 = se("log-in", i0);
const s0 = [
        ["path", {
            d: "m16 17 5-5-5-5",
            key: "1bji2h"
        }],
        ["path", {
            d: "M21 12H9",
            key: "dn1m92"
        }],
        ["path", {
            d: "M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4",
            key: "1uf3rs"
        }]
    ],
    f0 = se("log-out", s0);
const o0 = [
        ["path", {
            d: "M20.985 12.486a9 9 0 1 1-9.473-9.472c.405-.022.617.46.402.803a6 6 0 0 0 8.268 8.268c.344-.215.825-.004.803.401",
            key: "kfwtm"
        }]
    ],
    r0 = se("moon", o0);
const d0 = [
        ["path", {
            d: "M9 18V5l12-2v13",
            key: "1jmyc2"
        }],
        ["circle", {
            cx: "6",
            cy: "18",
            r: "3",
            key: "fqmcym"
        }],
        ["circle", {
            cx: "18",
            cy: "16",
            r: "3",
            key: "1hluhg"
        }]
    ],
    m0 = se("music", d0);
const h0 = [
        ["path", {
            d: "M5 5a2 2 0 0 1 3.008-1.728l11.997 6.998a2 2 0 0 1 .003 3.458l-12 7A2 2 0 0 1 5 19z",
            key: "10ikf1"
        }]
    ],
    v0 = se("play", h0);
const g0 = [
        ["path", {
            d: "m2 9 3-3 3 3",
            key: "1ltn5i"
        }],
        ["path", {
            d: "M13 18H7a2 2 0 0 1-2-2V6",
            key: "1r6tfw"
        }],
        ["path", {
            d: "m22 15-3 3-3-3",
            key: "4rnwn2"
        }],
        ["path", {
            d: "M11 6h6a2 2 0 0 1 2 2v10",
            key: "2f72bc"
        }]
    ],
    y0 = se("repeat-2", g0);
const p0 = [
        ["path", {
            d: "M4.5 16.5c-1.5 1.26-2 5-2 5s3.74-.5 5-2c.71-.84.7-2.13-.09-2.91a2.18 2.18 0 0 0-2.91-.09z",
            key: "m3kijz"
        }],
        ["path", {
            d: "m12 15-3-3a22 22 0 0 1 2-3.95A12.88 12.88 0 0 1 22 2c0 2.72-.78 7.5-6 11a22.35 22.35 0 0 1-4 2z",
            key: "1fmvmk"
        }],
        ["path", {
            d: "M9 12H4s.55-3.03 2-4c1.62-1.08 5 0 5 0",
            key: "1f8sc4"
        }],
        ["path", {
            d: "M12 15v5s3.03-.55 4-2c1.08-1.62 0-5 0-5",
            key: "qeys4"
        }]
    ],
    S0 = se("rocket", p0);
const b0 = [
        ["path", {
            d: "M14.536 21.686a.5.5 0 0 0 .937-.024l6.5-19a.496.496 0 0 0-.635-.635l-19 6.5a.5.5 0 0 0-.024.937l7.93 3.18a2 2 0 0 1 1.112 1.11z",
            key: "1ffxy3"
        }],
        ["path", {
            d: "m21.854 2.147-10.94 10.939",
            key: "12cjpa"
        }]
    ],
    Ms = se("send", b0);
const N0 = [
        ["path", {
            d: "M9.671 4.136a2.34 2.34 0 0 1 4.659 0 2.34 2.34 0 0 0 3.319 1.915 2.34 2.34 0 0 1 2.33 4.033 2.34 2.34 0 0 0 0 3.831 2.34 2.34 0 0 1-2.33 4.033 2.34 2.34 0 0 0-3.319 1.915 2.34 2.34 0 0 1-4.659 0 2.34 2.34 0 0 0-3.32-1.915 2.34 2.34 0 0 1-2.33-4.033 2.34 2.34 0 0 0 0-3.831A2.34 2.34 0 0 1 6.35 6.051a2.34 2.34 0 0 0 3.319-1.915",
            key: "1i5ecw"
        }],
        ["circle", {
            cx: "12",
            cy: "12",
            r: "3",
            key: "1v7zrd"
        }]
    ],
    em = se("settings", N0);
const E0 = [
        ["path", {
            d: "M20 13c0 5-3.5 7.5-7.66 8.95a1 1 0 0 1-.67-.01C7.5 20.5 4 18 4 13V6a1 1 0 0 1 1-1c2 0 4.5-1.2 6.24-2.72a1.17 1.17 0 0 1 1.52 0C14.51 3.81 17 5 19 5a1 1 0 0 1 1 1z",
            key: "oel41y"
        }]
    ],
    tm = se("shield", E0);
const T0 = [
        ["circle", {
            cx: "8",
            cy: "21",
            r: "1",
            key: "jimo8o"
        }],
        ["circle", {
            cx: "19",
            cy: "21",
            r: "1",
            key: "13723u"
        }],
        ["path", {
            d: "M2.05 2.05h2l2.66 12.42a2 2 0 0 0 2 1.58h9.78a2 2 0 0 0 1.95-1.57l1.65-7.43H5.12",
            key: "9zh506"
        }]
    ],
    x0 = se("shopping-cart", T0);
const z0 = [
        ["path", {
            d: "M11.017 2.814a1 1 0 0 1 1.966 0l1.051 5.558a2 2 0 0 0 1.594 1.594l5.558 1.051a1 1 0 0 1 0 1.966l-5.558 1.051a2 2 0 0 0-1.594 1.594l-1.051 5.558a1 1 0 0 1-1.966 0l-1.051-5.558a2 2 0 0 0-1.594-1.594l-5.558-1.051a1 1 0 0 1 0-1.966l5.558-1.051a2 2 0 0 0 1.594-1.594z",
            key: "1s2grr"
        }],
        ["path", {
            d: "M20 2v4",
            key: "1rf3ol"
        }],
        ["path", {
            d: "M22 4h-4",
            key: "gwowj6"
        }],
        ["circle", {
            cx: "4",
            cy: "20",
            r: "2",
            key: "6kqj1y"
        }]
    ],
    j0 = se("sparkles", z0);
const M0 = [
        ["path", {
            d: "M16 7h6v6",
            key: "box55l"
        }],
        ["path", {
            d: "m22 7-8.5 8.5-5-5L2 17",
            key: "1t1m79"
        }]
    ],
    D0 = se("trending-up", M0);
const A0 = [
        ["path", {
            d: "m21.73 18-8-14a2 2 0 0 0-3.48 0l-8 14A2 2 0 0 0 4 21h16a2 2 0 0 0 1.73-3",
            key: "wmoenq"
        }],
        ["path", {
            d: "M12 9v4",
            key: "juzpu7"
        }],
        ["path", {
            d: "M12 17h.01",
            key: "p32p05"
        }]
    ],
    _0 = se("triangle-alert", A0);
const O0 = [
        ["path", {
            d: "M12 4v16",
            key: "1654pz"
        }],
        ["path", {
            d: "M4 7V5a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v2",
            key: "e0r10z"
        }],
        ["path", {
            d: "M9 20h6",
            key: "s66wpe"
        }]
    ],
    R0 = se("type", O0);
const U0 = [
        ["path", {
            d: "M12 3v12",
            key: "1x0j5s"
        }],
        ["path", {
            d: "m17 8-5-5-5 5",
            key: "7q97r8"
        }],
        ["path", {
            d: "M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4",
            key: "ih7n3h"
        }]
    ],
    C0 = se("upload", U0);
const H0 = [
        ["path", {
            d: "M2 21a8 8 0 0 1 13.292-6",
            key: "bjp14o"
        }],
        ["circle", {
            cx: "10",
            cy: "8",
            r: "5",
            key: "o932ke"
        }],
        ["path", {
            d: "m16 19 2 2 4-4",
            key: "1b14m6"
        }]
    ],
    ei = se("user-round-check", H0);
const q0 = [
        ["path", {
            d: "m14.305 19.53.923-.382",
            key: "3m78fa"
        }],
        ["path", {
            d: "m15.228 16.852-.923-.383",
            key: "npixar"
        }],
        ["path", {
            d: "m16.852 15.228-.383-.923",
            key: "5xggr7"
        }],
        ["path", {
            d: "m16.852 20.772-.383.924",
            key: "dpfhf9"
        }],
        ["path", {
            d: "m19.148 15.228.383-.923",
            key: "1reyyz"
        }],
        ["path", {
            d: "m19.53 21.696-.382-.924",
            key: "1goivc"
        }],
        ["path", {
            d: "M2 21a8 8 0 0 1 10.434-7.62",
            key: "1yezr2"
        }],
        ["path", {
            d: "m20.772 16.852.924-.383",
            key: "htqkph"
        }],
        ["path", {
            d: "m20.772 19.148.924.383",
            key: "9w9pjp"
        }],
        ["circle", {
            cx: "10",
            cy: "8",
            r: "5",
            key: "o932ke"
        }],
        ["circle", {
            cx: "18",
            cy: "18",
            r: "3",
            key: "1xkwt0"
        }]
    ],
    lm = se("user-round-cog", q0);
const B0 = [
        ["path", {
            d: "M2 21a8 8 0 0 1 13.292-6",
            key: "bjp14o"
        }],
        ["circle", {
            cx: "10",
            cy: "8",
            r: "5",
            key: "o932ke"
        }],
        ["path", {
            d: "M19 16v6",
            key: "tddt3s"
        }],
        ["path", {
            d: "M22 19h-6",
            key: "vcuq98"
        }]
    ],
    Oa = se("user-round-plus", B0);
const L0 = [
        ["circle", {
            cx: "12",
            cy: "8",
            r: "5",
            key: "1hypcn"
        }],
        ["path", {
            d: "M20 21a8 8 0 0 0-16 0",
            key: "rfgkzh"
        }]
    ],
    am = se("user-round", L0);
const k0 = [
        ["path", {
            d: "M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2",
            key: "975kel"
        }],
        ["circle", {
            cx: "12",
            cy: "7",
            r: "4",
            key: "17ys0d"
        }]
    ],
    Rs = se("user", k0);
const Y0 = [
        ["path", {
            d: "m16 13 5.223 3.482a.5.5 0 0 0 .777-.416V7.87a.5.5 0 0 0-.752-.432L16 10.5",
            key: "ftymec"
        }],
        ["rect", {
            x: "2",
            y: "6",
            width: "14",
            height: "12",
            rx: "2",
            key: "158x01"
        }]
    ],
    Kd = se("video", Y0);
const G0 = [
        ["path", {
            d: "M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.106-3.105c.32-.322.863-.22.983.218a6 6 0 0 1-8.259 7.057l-7.91 7.91a1 1 0 0 1-2.999-3l7.91-7.91a6 6 0 0 1 7.057-8.259c.438.12.54.662.219.984z",
            key: "1ngwbx"
        }]
    ],
    X0 = se("wrench", G0);
const Q0 = [
        ["path", {
            d: "M18 6 6 18",
            key: "1bl5f8"
        }],
        ["path", {
            d: "m6 6 12 12",
            key: "d8bk6v"
        }]
    ],
    Ds = se("x", Q0);
const V0 = [
        ["path", {
            d: "M4 14a1 1 0 0 1-.78-1.63l9.9-10.2a.5.5 0 0 1 .86.46l-1.92 6.02A1 1 0 0 0 13 10h7a1 1 0 0 1 .78 1.63l-9.9 10.2a.5.5 0 0 1-.86-.46l1.92-6.02A1 1 0 0 0 11 14z",
            key: "1xq2db"
        }]
    ],
    As = se("zap", V0),
    Jd = {
        en: {
            title: "TikTok Enhancer",
            subtitle: "Makes TikTok Easier",
            guest: "Guest",
            notLoggedIn: "Not logged in",
            statusActive: "ACTIVE",
            statusDisabled: "DISABLED",
            settings: "Settings",
            fps60: "1080/60 FPS Bypass (Old Method)",
            fps60Desc: "Removes quality and fps limits",
            promoVideos: "Promo Videos",
            promoVideosDesc: "Upload with added sound",
            authorStats: "Author Statistics",
            authorStatsDesc: "Show profile analytics",
            videoStats: "Video Statistics",
            videoStatsDesc: "Show detailed video data",
            studioDarkMode: "Studio Dark Mode",
            studioDarkModeDesc: "Dark theme for TikTok Studio",
            hqUpload: "HQ Upload",
            hqUploadDesc: "Upload in maximum quality",
            originalDownload: "Original Download",
            originalDownloadDesc: "Download videos in original quality",
            enhancedStats: "Enhanced Statistics",
            enhancedStatsDesc: "More detailed and accurate info",
            authRequired: "Authentication Required",
            authDesc: "Subscribe to channels and enter your Telegram ID",
            authenticate: "Authenticate",
            telegramId: "Telegram User ID:",
            mustSubscribe: "You must be subscribed to both channels",
            getIdWith: "Get ID with @editingnews_bot",
            enterValidId: "⚠ Enter a valid User ID",
            authenticating: "⏲ Authenticating...",
            authSuccess: "Authentication Successful!",
            subscribeFirst: "⚠ Subscribe to channels first",
            authFailed: "Authentication failed",
            couldntConnect: "⚠ Couldn't connect to server",
            sessionExpired: "⚠ Session expired, please log in again",
            partnershipFeatures: "Premium",
            partnershipDesc: "Get Premium to unlock exclusive features",
            partnershipBenefit: "Unlock all Premium features",
            addSignature: "Add Watermark",
            addSignatureDesc: "Show authorship of the method in description",
            contactManager: "Contact manager",
            close: "Close",
            manager: "Manager",
            videoPatcher: "Video Patcher",
            selectVideo: "Click to select video",
            originalFps: "Original FPS",
            targetFps: "Target FPS",
            patchVideo: "Patch Video",
            processing: "Processing...",
            invalidVideoFile: "Please select a valid video file",
            processingError: "Error processing video",
            notSubscribed: "Not subscribed",
            subscriptionRequired: "Subscription Required",
            subscriptionDesc: "Subscribe to both channels to unlock all features",
            checkSubscription: "Check Subscription",
            notSubscribedYet: "Not subscribed to both channels yet",
            unlock: "Unlock",
            login: "Login",
            loginWithTelegram: "Login with Telegram",
            authDescTelegram: "Subscribe to channels and login via Telegram",
            waitingForAuth: "Waiting for authorization...",
            clickStartInBot: "Click START in the bot to complete login",
            authTimeout: "Authorization timeout. Please try again.",
            connectionError: "Connection error. Please try again.",
            reopenLink: "Open link again",
            cancel: "Cancel",
            tryAgain: "Try Again",
            premiumBenefit1: "• Disable watermark on uploads",
            premiumBenefit2: "• Enhanced & accurate statistics",
            premiumBenefit3: "• Early access to Studio Method",
            premiumBenefit4: "• All future premium features",
            saleEnds: "Sale ends in",
            perMonth: "1 Month",
            per3Months: "3 Months",
            popular: "POPULAR",
            save: "SAVE",
            day: "day",
            mo: "mo",
            boughtToday: "people bought today",
            buyInBot: "Buy",
            applyPartnership: "Get Partner",
            or: "or",
            notPartnerToast: "Partner/Premium feature. Get access below.",
            studioMethodDesc: "New quality method is almost ready. Partner and Premium users get it first.",
            studioPartnerNote: "Early access for Partner/Premium",
            studioMethodLiveDesc: "TikTok won't re-compress your video. Original quality preserved.",
            studioMethodAllDesc: "Max quality upload for everyone",
            studioPartnerOnly: "Partner/Premium only",
            studioTagDev: "SOON",
            dailyRemaining: "left today",
            dailyLimitReached: "Limit reached",
            weeklyRemaining: "left this week",
            weeklyLimitReached: "Weekly limit reached",
            comingSoon: "SOON",
            badgeOwner: "Owner",
            badgeEditingPremium: "Editing Premium",
            badgePartner: "Partner",
            badgePremium: "Premium",
            badgeEditing: "Editing Team",
            badgeUser: "User",
            clearCookies: "Fix Upload",
            clearCookiesDesc: "Clear TTWID cookie if video won't upload",
            cookieCleared: "TTWID cleared, try uploading again",
            cookieNotFound: "TTWID cookie not found",
            tools: "Tools",
            repostRemover: "Repost Remover",
            repostRemoverDesc: "Remove all reposts from your profile",
            repostFilterKeywords: "Filter by keywords (uncheck to remove all)",
            repostKeywordsPlaceholder: "e.g. cat, memecoin",
            repostInterval: "Interval (sec)",
            repostIntervalRange: "Min – max",
            repostIntervalSet: "Fixed values",
            repostPagePause: "Pause between pages (s)",
            repostReport: "Report",
            repostStart: "Start Removing Reposts",
            repostSignInFirst: "Sign in to TikTok first",
            repostPanelTitle: "Repost Remover",
            repostPreparing: "Preparing…",
            repostPaused: "Paused",
            repostResuming: "Resuming…",
            repostBtnPause: "Pause",
            repostBtnResume: "Resume",
            repostBtnDownload: "Download report",
            repostWaiting: "Identifying your account…",
            repostListing: "Listing reposts…",
            repostPageRemoving: "Page $1$: removing $2$ of $3$ items…",
            repostDone: "Done! All reposts processed.",
            repostNone: "No reposts found.",
            repostErrorNoAccount: "Could not identify your account. Reload TikTok and try again.",
            repostErrorNotLoggedIn: "You were redirected to For You because you're not logged in. Please log in to TikTok, then try again.",
            repostErrorRemove: "Error removing $1$. Check console.",
            repostClose: "Close",
            repostStatsPages: "Pages",
            repostStatsRemoved: "Removed",
            repostStatsListed: "Listed",
            repostStatsFailed: "Failed",
            repostStoppedFailures: "Stopped: $1$ consecutive failures.",
            repostBetweenPages: "Pause before next page…",
            tabHome: "Home",
            tabVpn: "VPN",
            tabSettings: "Settings",
            tabTools: "Tools",
            tabProfile: "Profile",
            logout: "Log out",
            hqDisabledByFps: "HQ Upload disabled — 60 FPS is active",
            fpsDisabledByHq: "60 FPS disabled — HQ Upload is active",
            activeMethod: "Active method: ",
            vpnMovedTitle: "VPN",
            vpnMovedDesc: "VPN has moved to its own dedicated extension for better security.",
            vpnMovedButton: "Get Editing VPN",
            vpnMovedHint: "Install Editing VPN separately and log in with your Editing News account."
        },
        ru: {
            title: "TikTok Enhancer",
            subtitle: "Делаем TikTok проще",
            guest: "Гость",
            notLoggedIn: "Не авторизован",
            statusActive: "АКТИВНО",
            statusDisabled: "ОТКЛЮЧЕНО",
            settings: "Настройки",
            fps60: "Обход 1080/60 FPS (Старый метод)",
            fps60Desc: "Убирает ограничения качества и фпс",
            promoVideos: "Промо видео",
            promoVideosDesc: "Загрузка с добавленным звуком",
            authorStats: "Статистика автора",
            authorStatsDesc: "Показывать аналитику профиля",
            videoStats: "Статистика видео",
            videoStatsDesc: "Показывать подробные данные о видео",
            studioDarkMode: "Тёмный режим студии",
            studioDarkModeDesc: "Тёмная тема для TikTok Studio",
            hqUpload: "HQ загрузка",
            hqUploadDesc: "Загрузка в максимальном качестве",
            originalDownload: "Скачать оригинал",
            originalDownloadDesc: "Скачивание видео в оригинальном качестве",
            enhancedStats: "Улучшенная статистика",
            enhancedStatsDesc: "Более подробная и точная информация",
            authRequired: "Требуется аутентификация",
            authDesc: "Подпишитесь на каналы и введите ваш Telegram ID",
            authenticate: "Аутентифицировать",
            telegramId: "Telegram User ID:",
            mustSubscribe: "Вы должны быть подписаны на оба канала",
            getIdWith: "Получить ID с @editingnews_bot",
            enterValidId: "⚠ Введите действительный User ID",
            authenticating: "⏲ Аутентификация...",
            authSuccess: "Аутентификация успешна!",
            subscribeFirst: "⚠ Сначала подпишитесь на каналы",
            authFailed: "Аутентификация не удалась",
            couldntConnect: "⚠ Не удалось подключиться к серверу",
            sessionExpired: "⚠ Сессия истекла, войдите снова",
            partnershipFeatures: "Premium",
            partnershipDesc: "Получите Premium, чтобы разблокировать эксклюзивные функции",
            partnershipBenefit: "Разблокируйте все Premium-функции",
            addSignature: "Добавить подпись",
            addSignatureDesc: "Показывать авторство метода в описании",
            contactManager: "Написать менеджеру",
            close: "Закрыть",
            manager: "Менеджер",
            videoPatcher: "Патчер видео",
            selectVideo: "Нажмите чтобы выбрать видео",
            originalFps: "Оригинальный FPS",
            targetFps: "Целевой FPS",
            patchVideo: "Пропатчить видео",
            processing: "Обработка...",
            invalidVideoFile: "Выберите корректный видео файл",
            processingError: "Ошибка обработки видео",
            notSubscribed: "Не подписан",
            subscriptionRequired: "Требуется подписка",
            subscriptionDesc: "Подпишитесь на оба канала для доступа ко всем функциям",
            checkSubscription: "Проверить подписку",
            notSubscribedYet: "Вы ещё не подписаны на оба канала",
            unlock: "Разблокировать",
            login: "Войти",
            loginWithTelegram: "Войти через Telegram",
            authDescTelegram: "Подпишитесь на каналы и войдите через Telegram",
            waitingForAuth: "Ожидание авторизации...",
            clickStartInBot: "Нажмите START в боте для завершения входа",
            authTimeout: "Время авторизации истекло. Попробуйте снова.",
            connectionError: "Ошибка подключения. Попробуйте снова.",
            reopenLink: "Открыть ссылку снова",
            cancel: "Отмена",
            tryAgain: "Попробовать снова",
            premiumBenefit1: "• Убрать водяной знак при загрузке",
            premiumBenefit2: "• Улучшенная и точная статистика",
            premiumBenefit3: "• Ранний доступ к Studio Method",
            premiumBenefit4: "• Все будущие премиум функции",
            saleEnds: "Акция закончится через",
            perMonth: "1 Месяц",
            per3Months: "3 Месяца",
            popular: "ХИТ",
            save: "ВЫГОДА",
            day: "день",
            mo: "мес",
            boughtToday: "человек купили сегодня",
            buyInBot: "Купить",
            applyPartnership: "Получить Partner",
            or: "или",
            notPartnerToast: "Функция Partner/Premium. Получите доступ ниже.",
            studioMethodDesc: "Новый метод качества почти готов. Пользователи Partner и Premium получат первыми.",
            studioPartnerNote: "Ранний доступ для Partner/Premium",
            studioMethodLiveDesc: "TikTok не пережимает видео. Оригинальное качество сохраняется.",
            studioMethodAllDesc: "Загрузка в максимальном качестве для всех",
            studioPartnerOnly: "Только для Partner/Premium",
            studioTagDev: "СКОРО",
            dailyRemaining: "осталось сегодня",
            dailyLimitReached: "Лимит исчерпан",
            weeklyRemaining: "осталось на этой неделе",
            weeklyLimitReached: "Недельный лимит исчерпан",
            comingSoon: "СКОРО",
            badgeOwner: "Овнер",
            badgeEditingPremium: "Editing Premium",
            badgePartner: "Partner",
            badgePremium: "Premium",
            badgeEditing: "Editing Команда",
            badgeUser: "Пользователь",
            clearCookies: "Фикс загрузки",
            clearCookiesDesc: "Очистить TTWID если видео не загружается",
            cookieCleared: "TTWID очищен, попробуйте загрузить снова",
            cookieNotFound: "Куки TTWID не найдены",
            tools: "Инструменты",
            repostRemover: "Удаление репостов",
            repostRemoverDesc: "Удалить все репосты с вашего профиля",
            repostFilterKeywords: "Фильтр по ключевым словам (снимите для удаления всех)",
            repostKeywordsPlaceholder: "напр. кот, мемкоин",
            repostInterval: "Интервал (сек)",
            repostIntervalRange: "Мин – макс",
            repostIntervalSet: "Фикс. значения",
            repostPagePause: "Пауза между страницами (с)",
            repostReport: "Отчёт",
            repostStart: "Удалить все репосты",
            repostSignInFirst: "Сначала войдите в TikTok",
            repostPanelTitle: "Удаление репостов",
            repostPreparing: "Подготовка…",
            repostPaused: "Пауза",
            repostResuming: "Возобновление…",
            repostBtnPause: "Пауза",
            repostBtnResume: "Продолжить",
            repostBtnDownload: "Скачать отчёт",
            repostWaiting: "Определяем ваш аккаунт…",
            repostListing: "Получаем список репостов…",
            repostPageRemoving: "Страница $1$: удаляем $2$ из $3$…",
            repostDone: "Готово! Все репосты обработаны.",
            repostNone: "Репосты не найдены.",
            repostErrorNoAccount: "Не удалось определить аккаунт. Перезагрузите TikTok и попробуйте снова.",
            repostErrorNotLoggedIn: "Вы попали на Рекомендации — вы не вошли. Войдите в TikTok и попробуйте снова.",
            repostErrorRemove: "Ошибка удаления $1$. Смотрите консоль.",
            repostClose: "Закрыть",
            repostStatsPages: "Страницы",
            repostStatsRemoved: "Удалено",
            repostStatsListed: "Найдено",
            repostStatsFailed: "Ошибки",
            repostStoppedFailures: "Остановлено: $1$ ошибок подряд.",
            repostBetweenPages: "Пауза перед следующей страницей…",
            tabHome: "Главная",
            tabVpn: "ВПН",
            tabSettings: "Настройки",
            tabTools: "Утилиты",
            tabProfile: "Профиль",
            logout: "Выйти",
            hqDisabledByFps: "HQ загрузка выключена — 60 FPS активен",
            fpsDisabledByHq: "60 FPS выключен — HQ загрузка активна",
            activeMethod: "Активный метод: ",
            vpnMovedTitle: "ВПН",
            vpnMovedDesc: "ВПН перенесён в отдельное расширение для лучшей безопасности.",
            vpnMovedButton: "Установить Editing VPN",
            vpnMovedHint: "Установите Editing VPN отдельно и войдите через аккаунт Телеграм."
        }
    };

function w0() {
    const [f, b] = L.useState("en"), [N, o] = L.useState("dark"), [h, z] = L.useState(!1);
    L.useEffect(() => {
        et.get(["language", "theme"]).then(M => {
            b(M.language || "en"), o(M.theme || "dark")
        })
    }, []);
    const C = L.useCallback(async M => {
            M !== f && (z(!0), await new Promise(X => setTimeout(X, 150)), b(M), await et.set({
                language: M
            }), await new Promise(X => setTimeout(X, 20)), z(!1))
        }, [f]),
        R = L.useCallback(() => {
            C(f === "en" ? "ru" : "en")
        }, [f, C]),
        _ = L.useCallback(async M => {
            o(M), await et.set({
                theme: M
            })
        }, []),
        S = L.useCallback(() => {
            _(N === "dark" ? "light" : "dark")
        }, [N, _]),
        q = L.useCallback(M => Jd[f][M] || Jd.en[M] || M, [f]);
    return {
        language: f,
        setLanguage: C,
        toggleLanguage: R,
        theme: N,
        setTheme: _,
        toggleTheme: S,
        t: q,
        isChanging: h
    }
}
const Wd = 12e4,
    Z0 = 2e3,
    K0 = [{
        name: "@editing_news",
        url: "https://t.me/editing_news"
    }, {
        name: "@lexuof",
        url: "https://t.me/lexuof"
    }];

function J0({
    onClose: f,
    isLoggedIn: b,
    t: N
}) {
    const [o, h] = L.useState("checking"), [z, C] = L.useState(""), R = L.useRef(null), _ = L.useRef(null), S = L.useRef(!1), q = L.useRef(null);
    L.useEffect(() => () => {
        R.current && clearTimeout(R.current), _.current && clearInterval(_.current)
    }, []), L.useEffect(() => {
        if (b) {
            h("idle");
            return
        }
        chrome.storage.session.get(["pendingAuthToken", "pendingBotLink", "authExpiry"], J => {
            const ze = J.pendingAuthToken,
                F = J.pendingBotLink,
                Re = J.authExpiry;
            ze && Re && Date.now() < Re ? (q.current = F || null, h("waiting"), X(ze, Re)) : h("idle")
        })
    }, []), L.useEffect(() => {
        b && o === "waiting" && M()
    }, [b]);

    function M() {
        S.current || (S.current = !0, _.current && clearInterval(_.current), R.current && clearTimeout(R.current), h("success"), setTimeout(() => f(), 1200))
    }

    function X(J, ze) {
        _.current && clearInterval(_.current), _.current = setInterval(async () => {
            if (S.current || Date.now() > ze) {
                clearInterval(_.current), _.current = null;
                return
            }
            try {
                const F = await Fu.authCheck(J);
                F.confirmed && F.session && F.user && (clearInterval(_.current), _.current = null, await et.set({
                    session: F.session,
                    encKey: F.encKey || "",
                    userId: F.user.id,
                    username: F.user.username || "",
                    firstName: F.user.firstName || "",
                    avatar: F.user.avatar || "",
                    isSubscribed: F.subscribed ?? !1,
                    isPartner: F.isPartner ?? !1,
                    isPremium: F.isPremium ?? !1,
                    badges: F.badges ?? [],
                    studioMethodMode: F.studioMethodMode ?? "off",
                    canDisableWatermark: F.canDisableWatermark ?? !1,
                    allowPartnershipNoWatermark: F.allowPartnershipNoWatermark ?? !1,
                    featureSettings: {
                        addSignature: !0,
                        fps60: !0,
                        promoVideos: !0,
                        authorStats: !0,
                        videoStats: !0,
                        studioDarkMode: !0,
                        enhancedStats: !1,
                        hqUpload: !0,
                        originalDownload: !1
                    }
                }), M())
            } catch {}
        }, Z0)
    }
    const w = () => {
            S.current = !1, h("waiting"), C(""), _.current && clearInterval(_.current), R.current = setTimeout(() => {
                S.current || (h("error"), C(N("authTimeout")), _.current && clearInterval(_.current))
            }, Wd), chrome.runtime.sendMessage({
                action: "startAuth"
            }, J => {
                if (chrome.runtime.lastError || !J || J?.error) {
                    S.current || (h("error"), C(N("connectionError")), R.current && clearTimeout(R.current));
                    return
                }
                const {
                    token: F,
                    botLink: Re
                } = J;
                if (q.current = Re || null, F) {
                    const W = Date.now() + Wd;
                    X(F, W)
                }
            })
        },
        V = () => {
            S.current = !1, h("idle"), C(""), q.current = null, R.current && clearTimeout(R.current), _.current && clearInterval(_.current)
        },
        K = () => {
            q.current && chrome.tabs.create({
                url: q.current
            })
        };
    if (o === "checking") return c.jsx("div", {
        className: "modal-overlay",
        onClick: f,
        children: c.jsx("div", {
            className: "auth-modal",
            onClick: J => J.stopPropagation(),
            children: c.jsx("button", {
                className: "modal-close",
                onClick: f,
                children: c.jsx(Ds, {
                    size: 16
                })
            })
        })
    });
    const ae = {
        idle: Ms,
        waiting: Pu,
        success: js,
        error: Pd
    } [o];
    return c.jsx("div", {
        className: "modal-overlay",
        onClick: f,
        children: c.jsxs("div", {
            className: "auth-modal",
            onClick: J => J.stopPropagation(),
            children: [c.jsx("button", {
                className: "modal-close",
                onClick: f,
                children: c.jsx(Ds, {
                    size: 16
                })
            }), c.jsx("div", {
                className: `auth-icon ${o}`,
                children: c.jsx(ae, {
                    size: 36,
                    className: o === "waiting" ? "auth-spin" : ""
                })
            }), c.jsxs("h2", {
                className: "auth-title",
                children: [o === "idle" && N("authRequired"), o === "waiting" && N("waitingForAuth"), o === "success" && N("authSuccess"), o === "error" && N("authFailed")]
            }), o === "idle" && c.jsxs(c.Fragment, {
                children: [c.jsx("p", {
                    className: "auth-desc",
                    children: N("authDescTelegram")
                }), c.jsx("div", {
                    className: "auth-channels",
                    children: K0.map(J => c.jsx("button", {
                        className: "channel-btn",
                        onClick: () => chrome.tabs.create({
                            url: J.url
                        }),
                        children: J.name
                    }, J.name))
                }), c.jsxs("button", {
                    className: "auth-btn",
                    onClick: w,
                    children: [c.jsx(Ms, {
                        size: 16
                    }), N("loginWithTelegram")]
                })]
            }), o === "waiting" && c.jsxs(c.Fragment, {
                children: [c.jsx("p", {
                    className: "auth-desc",
                    children: N("clickStartInBot")
                }), q.current && c.jsxs("button", {
                    className: "auth-reopen-btn",
                    onClick: K,
                    children: [c.jsx(Os, {
                        size: 14
                    }), N("reopenLink")]
                })]
            }), o === "error" && c.jsxs(c.Fragment, {
                children: [c.jsx("p", {
                    className: "auth-error",
                    children: z
                }), c.jsx("button", {
                    className: "auth-btn",
                    onClick: V,
                    children: N("tryAgain")
                })]
            }), c.jsx("p", {
                className: "auth-footer",
                children: N("mustSubscribe")
            })]
        })
    })
}
const W0 = {
    owner: {
        icon: ti,
        className: "badge-icon badge-owner",
        titleKey: "badgeOwner"
    },
    partner: {
        icon: ei,
        className: "badge-icon badge-editing-partnership",
        titleKey: "badgePartner"
    },
    premium: {
        icon: Oa,
        className: "badge-icon badge-editing-plus",
        titleKey: "badgePremium"
    },
    editing_plus: {
        icon: Oa,
        className: "badge-icon badge-editing-plus",
        titleKey: "badgePremium"
    },
    editing_premium: {
        icon: Oa,
        className: "badge-icon badge-editing-plus",
        titleKey: "badgePremium"
    },
    editing_partnership: {
        icon: ei,
        className: "badge-icon badge-editing-partnership",
        titleKey: "badgePartner"
    },
    editing: {
        icon: lm,
        className: "badge-icon badge-editing",
        titleKey: "badgeEditing"
    }
};

function $0({
    state: f,
    language: b,
    onLanguageToggle: N,
    onProfileClick: o,
    onAuthClick: h,
    t: z
}) {
    const C = f.firstName || f.username || "—",
        [R, _] = L.useState(!1),
        [S, q] = L.useState(!1);
    L.useEffect(() => {
        _(!1), q(!1)
    }, [f.avatar]);
    const M = L.useCallback(V => {
            V?.complete && V.naturalWidth > 0 && _(!0)
        }, [f.avatar]),
        X = f.avatar && !S,
        w = !f.avatar || S || !R;
    return c.jsxs("div", {
        className: "top-bar",
        children: [f.isLoggedIn ? c.jsxs("div", {
            className: "user-section",
            children: [c.jsx("div", {
                className: "avatar-wrapper",
                onClick: o,
                title: z("tabProfile"),
                children: c.jsxs("div", {
                    className: "avatar",
                    children: [X && c.jsx("img", {
                        ref: M,
                        src: f.avatar,
                        alt: "",
                        className: `avatar-img${R?" loaded":""}`,
                        onLoad: () => _(!0),
                        onError: () => q(!0)
                    }), w && c.jsx("span", {
                        className: "avatar-initials",
                        children: C.slice(0, 2).toUpperCase()
                    })]
                })
            }), c.jsxs("div", {
                children: [c.jsxs("div", {
                    className: "user-name",
                    children: [C, f.badges && f.badges.length > 0 ? c.jsx("span", {
                        className: "user-badges",
                        children: f.badges.map(V => {
                            const K = W0[V];
                            if (!K) return null;
                            const ae = K.icon;
                            return c.jsx("span", {
                                title: z(K.titleKey),
                                children: c.jsx(ae, {
                                    size: 12,
                                    className: K.className
                                })
                            }, V)
                        })
                    }) : c.jsx("span", {
                        title: z("badgeUser"),
                        children: c.jsx(am, {
                            size: 12,
                            className: "badge-icon badge-regular"
                        })
                    })]
                }), c.jsxs("div", {
                    className: "user-id",
                    children: ["ID: ", f.userId || "—"]
                }), !f.isSubscribed && c.jsxs("div", {
                    className: "user-sub-warning",
                    children: [c.jsx(_0, {
                        size: 10
                    }), z("notSubscribed")]
                })]
            })]
        }) : c.jsxs("div", {
            className: "user-section guest",
            children: [c.jsx("div", {
                className: "avatar-wrapper",
                onClick: h,
                title: z("login"),
                children: c.jsx("div", {
                    className: "avatar guest-avatar",
                    children: c.jsx(Rs, {
                        size: 18
                    })
                })
            }), c.jsxs("div", {
                children: [c.jsx("div", {
                    className: "user-name",
                    children: z("guest")
                }), c.jsx("div", {
                    className: "user-id",
                    children: z("notLoggedIn")
                })]
            })]
        }), c.jsx("div", {
            className: "header-controls",
            children: c.jsx("div", {
                className: "control-btn",
                onClick: N,
                title: "Switch language",
                children: b.toUpperCase()
            })
        })]
    })
}

function Ra({
    active: f,
    onClick: b,
    mini: N = !1,
    disabled: o = !1
}) {
    const h = N ? `mini-toggle ${f?"active":""} ${o?"disabled":""}` : `toggle ${f?"active":""} ${o?"disabled":""}`,
        z = N ? "mini-toggle-slider" : "toggle-slider";
    return c.jsx("div", {
        className: h,
        onClick: o ? void 0 : b,
        children: c.jsx("div", {
            className: z
        })
    })
}
const F0 = [{
    key: "fps60",
    icon: c.jsx(t0, {
        size: 16
    }),
    titleKey: "fps60",
    descKey: "fps60Desc"
}, {
    key: "promoVideos",
    icon: c.jsx(m0, {
        size: 16
    }),
    titleKey: "promoVideos",
    descKey: "promoVideosDesc"
}, {
    key: "authorStats",
    icon: c.jsx(Id, {
        size: 16
    }),
    titleKey: "authorStats",
    descKey: "authorStatsDesc"
}, {
    key: "videoStats",
    icon: c.jsx(D0, {
        size: 16
    }),
    titleKey: "videoStats",
    descKey: "videoStatsDesc"
}, {
    key: "studioDarkMode",
    icon: c.jsx(r0, {
        size: 16
    }),
    titleKey: "studioDarkMode",
    descKey: "studioDarkModeDesc",
    comingSoon: !0
}];

function I0({
    t: f,
    features: b,
    onToggle: N,
    isVerified: o = !0,
    onAuthClick: h
}) {
    return c.jsxs("div", {
        className: "settings-section",
        children: [c.jsxs("div", {
            className: "section-title",
            children: [c.jsx(em, {
                size: 14
            }), " ", f("settings")]
        }), F0.map(z => {
            const C = !o,
                R = z.comingSoon;
            return c.jsxs("div", {
                className: `setting-item ${R?"setting-coming-soon":""}`,
                style: {
                    position: "relative",
                    overflow: "hidden"
                },
                onClick: C && !R ? h : void 0,
                children: [C && !R && c.jsx("div", {
                    className: "lock-overlay",
                    onClick: h,
                    children: c.jsx(Ct, {
                        size: 16
                    })
                }), c.jsx("div", {
                    className: "setting-icon",
                    children: z.icon
                }), c.jsxs("div", {
                    className: "setting-content",
                    children: [c.jsxs("h4", {
                        children: [f(z.titleKey), R && c.jsx("span", {
                            className: "coming-soon-tag",
                            children: f("comingSoon")
                        })]
                    }), c.jsx("p", {
                        children: f(z.descKey)
                    })]
                }), c.jsx(Ra, {
                    active: R ? !1 : b[z.key],
                    onClick: C || R ? void 0 : () => N(z.key),
                    mini: !0,
                    disabled: C || R
                })]
            }, z.key)
        })]
    })
}

function P0() {
    const f = L.useRef(null),
        b = L.useRef(null),
        N = L.useRef(null),
        [o, h] = L.useState(!1);
    return L.useEffect(() => {
        const z = document.querySelector(".container");
        if (!z) return;
        const C = () => {
            const R = z.scrollHeight,
                _ = z.clientHeight,
                S = z.scrollTop,
                q = R - _ > 2;
            if (o !== q && h(q), !q) return;
            const M = f.current,
                X = b.current;
            if (!M || !X) return;
            const w = M.clientHeight,
                V = Math.max(Math.floor(_ / R * w), 30);
            X.style.height = `${V}px`;
            const K = w - V,
                ae = Math.max(1, R - _),
                J = Math.min(K, Math.max(0, S / ae * K));
            X.style.transform = `translateY(${J}px)`;
            const ze = f.current;
            ze && (ze.style.opacity = "1", N.current && window.clearTimeout(N.current), N.current = window.setTimeout(() => {
                f.current && (f.current.style.opacity = "0")
            }, 800))
        };
        return C(), z.addEventListener("scroll", C, {
            passive: !0
        }), window.addEventListener("resize", C), () => {
            z.removeEventListener("scroll", C), window.removeEventListener("resize", C), N.current && window.clearTimeout(N.current)
        }
    }, [o]), o ? c.jsx("div", {
        ref: f,
        "aria-hidden": "true",
        className: "overlay-scrollbar",
        children: c.jsx("div", {
            ref: b,
            className: "overlay-scrollbar-thumb"
        })
    }) : null
}
const ev = [{
        id: "vpn",
        icon: tm,
        labelKey: "tabVpn"
    }, {
        id: "settings",
        icon: em,
        labelKey: "tabSettings"
    }],
    tv = [{
        id: "tools",
        icon: X0,
        labelKey: "tabTools"
    }, {
        id: "profile",
        icon: Rs,
        labelKey: "tabProfile"
    }];

function lv({
    activeTab: f,
    onTabChange: b,
    t: N
}) {
    return c.jsxs("nav", {
        className: "bottom-nav",
        children: [c.jsx("div", {
            className: "bottom-nav-side",
            children: ev.map(({
                id: o,
                icon: h,
                labelKey: z
            }) => c.jsxs("button", {
                className: `bottom-nav-item ${f===o?"active":""}`,
                onClick: () => b(o),
                children: [c.jsx(h, {
                    size: 20,
                    strokeWidth: 1.5
                }), c.jsx("span", {
                    className: "bottom-nav-label",
                    children: N(z)
                })]
            }, o))
        }), c.jsx("button", {
            className: `bottom-nav-center ${f==="home"?"active":""}`,
            onClick: () => b("home"),
            children: c.jsx(a0, {
                size: 22,
                strokeWidth: 1.5
            })
        }), c.jsx("div", {
            className: "bottom-nav-side",
            children: tv.map(({
                id: o,
                icon: h,
                labelKey: z
            }) => c.jsxs("button", {
                className: `bottom-nav-item ${f===o?"active":""}`,
                onClick: () => b(o),
                children: [c.jsx(h, {
                    size: 20,
                    strokeWidth: 1.5
                }), c.jsx("span", {
                    className: "bottom-nav-label",
                    children: N(z)
                })]
            }, o))
        })]
    })
}

function av({
    t: f
}) {
    const b = () => {
        chrome.tabs.create({
            url: "https://editingnews.com/vpn"
        })
    };
    return c.jsx("div", {
        className: "vpn-page",
        children: c.jsxs("div", {
            className: "vpn-main",
            style: {
                gap: 20
            },
            children: [c.jsxs("div", {
                className: "vpn-hero",
                style: {
                    marginTop: 8
                },
                children: [c.jsx("div", {
                    style: {
                        marginBottom: 8
                    },
                    children: c.jsx(tm, {
                        size: 40,
                        style: {
                            color: "rgba(255,255,255,0.55)"
                        }
                    })
                }), c.jsx("div", {
                    className: "vpn-hero-name",
                    children: f("vpnMovedTitle")
                }), c.jsx("div", {
                    className: "vpn-hero-meta",
                    style: {
                        textAlign: "center",
                        maxWidth: 220,
                        lineHeight: 1.5
                    },
                    children: f("vpnMovedDesc")
                })]
            }), c.jsxs("button", {
                className: "vpn-button",
                onClick: b,
                children: [c.jsx(Os, {
                    size: 14
                }), f("vpnMovedButton")]
            }), c.jsx("div", {
                className: "vpn-subtitle",
                style: {
                    textAlign: "center"
                },
                children: f("vpnMovedHint")
            })]
        })
    })
}
const nv = "/assets/retiktok-BbePp16p.png",
    uv = "/assets/editingnews-75vpX1cA.png",
    iv = {
        owner: {
            icon: ti,
            className: "badge-icon badge-owner",
            titleKey: "badgeOwner"
        },
        partner: {
            icon: ei,
            className: "badge-icon badge-editing-partnership",
            titleKey: "badgePartner"
        },
        premium: {
            icon: Oa,
            className: "badge-icon badge-editing-plus",
            titleKey: "badgePremium"
        },
        editing_plus: {
            icon: Oa,
            className: "badge-icon badge-editing-plus",
            titleKey: "badgePremium"
        },
        editing_premium: {
            icon: Oa,
            className: "badge-icon badge-editing-plus",
            titleKey: "badgePremium"
        },
        editing_partnership: {
            icon: ei,
            className: "badge-icon badge-editing-partnership",
            titleKey: "badgePartner"
        },
        editing: {
            icon: lm,
            className: "badge-icon badge-editing",
            titleKey: "badgeEditing"
        }
    },
    cv = [{
        label: "re:TikTok",
        url: "https://t.me/retiktok_bot",
        logo: nv
    }, {
        label: "Editing News",
        url: "https://t.me/editing_news",
        logo: uv
    }];

function sv({
    state: f,
    onLogout: b,
    onAuthClick: N,
    version: o,
    t: h
}) {
    const z = f.firstName || f.username || "—",
        [C, R] = L.useState(!1),
        [_, S] = L.useState(!1),
        q = L.useCallback(w => {
            w?.complete && w.naturalWidth > 0 && R(!0)
        }, [f.avatar]),
        M = f.avatar && !_,
        X = w => {
            chrome.tabs.create({
                url: w
            })
        };
    return c.jsxs("div", {
        className: "profile-page",
        children: [f.isLoggedIn ? c.jsxs("div", {
            className: "profile-card",
            children: [c.jsxs("div", {
                className: "profile-avatar",
                children: [M && c.jsx("img", {
                    ref: q,
                    src: f.avatar,
                    alt: "",
                    className: `profile-avatar-img${C?" loaded":""}`,
                    onLoad: () => R(!0),
                    onError: () => S(!0)
                }), (!M || !C) && c.jsx("span", {
                    className: "profile-avatar-initials",
                    children: z.slice(0, 2).toUpperCase()
                })]
            }), c.jsx("div", {
                className: "profile-name",
                children: z
            }), f.username && c.jsxs("div", {
                className: "profile-username",
                children: ["@", f.username]
            }), c.jsxs("div", {
                className: "profile-id",
                children: ["ID: ", f.userId || "—"]
            }), c.jsx("div", {
                className: "profile-badges",
                children: f.badges && f.badges.length > 0 ? f.badges.map(w => {
                    const V = iv[w];
                    if (!V) return null;
                    const K = V.icon;
                    return c.jsxs("div", {
                        className: "profile-badge-item",
                        children: [c.jsx(K, {
                            size: 13,
                            className: V.className
                        }), c.jsx("span", {
                            children: h(V.titleKey)
                        })]
                    }, w)
                }) : c.jsxs("div", {
                    className: "profile-badge-item",
                    children: [c.jsx(am, {
                        size: 13,
                        className: "badge-icon badge-regular"
                    }), c.jsx("span", {
                        children: h("badgeUser")
                    })]
                })
            }), c.jsxs("div", {
                className: `profile-status ${f.isSubscribed?"profile-status-active":"profile-status-inactive"}`,
                children: [c.jsx("span", {
                    className: "profile-status-dot"
                }), f.isSubscribed ? h("statusActive") : h("notSubscribed")]
            }), c.jsxs("button", {
                className: "profile-logout",
                onClick: b,
                children: [c.jsx(f0, {
                    size: 14
                }), h("logout")]
            })]
        }) : c.jsxs("div", {
            className: "profile-card profile-card-guest",
            children: [c.jsx("div", {
                className: "profile-avatar profile-avatar-guest",
                children: c.jsx(Rs, {
                    size: 28
                })
            }), c.jsx("div", {
                className: "profile-name",
                children: h("guest")
            }), c.jsx("div", {
                className: "profile-id",
                children: h("notLoggedIn")
            }), c.jsxs("button", {
                className: "profile-login",
                onClick: N,
                children: [c.jsx(c0, {
                    size: 14
                }), h("login")]
            })]
        }), c.jsx("div", {
            className: "profile-links",
            children: cv.map((w, V) => c.jsxs("div", {
                className: "profile-link-item",
                onClick: () => X(w.url),
                children: [c.jsx("img", {
                    src: w.logo,
                    alt: w.label,
                    className: "profile-link-logo"
                }), c.jsx("span", {
                    children: w.label
                }), c.jsx(Os, {
                    size: 10,
                    className: "profile-link-arrow"
                })]
            }, V))
        }), c.jsxs("div", {
            className: "profile-footer",
            children: [c.jsxs("div", {
                className: "profile-version-badge",
                children: ["v", o]
            }), c.jsx("div", {
                className: "profile-copyright",
                children: "© 2026 TikTok Enhancer"
            })]
        })]
    })
}
var pe;
(function (f) {
    f.LOAD = "LOAD", f.EXEC = "EXEC", f.FFPROBE = "FFPROBE", f.WRITE_FILE = "WRITE_FILE", f.READ_FILE = "READ_FILE", f.DELETE_FILE = "DELETE_FILE", f.RENAME = "RENAME", f.CREATE_DIR = "CREATE_DIR", f.LIST_DIR = "LIST_DIR", f.DELETE_DIR = "DELETE_DIR", f.ERROR = "ERROR", f.DOWNLOAD = "DOWNLOAD", f.PROGRESS = "PROGRESS", f.LOG = "LOG", f.MOUNT = "MOUNT", f.UNMOUNT = "UNMOUNT"
})(pe || (pe = {}));
const fv = (() => {
        let f = 0;
        return () => f++
    })(),
    ov = new Error("ffmpeg is not loaded, call `await ffmpeg.load()` first"),
    rv = new Error("called FFmpeg.terminate()");
class dv {
    #t = null;
    #a = {};
    #l = {};
    #n = [];
    #u = [];
    loaded = !1;
    #i = () => {
        this.#t && (this.#t.onmessage = ({
            data: {
                id: b,
                type: N,
                data: o
            }
        }) => {
            switch (N) {
            case pe.LOAD:
                this.loaded = !0, this.#a[b](o);
                break;
            case pe.MOUNT:
            case pe.UNMOUNT:
            case pe.EXEC:
            case pe.FFPROBE:
            case pe.WRITE_FILE:
            case pe.READ_FILE:
            case pe.DELETE_FILE:
            case pe.RENAME:
            case pe.CREATE_DIR:
            case pe.LIST_DIR:
            case pe.DELETE_DIR:
                this.#a[b](o);
                break;
            case pe.LOG:
                this.#n.forEach(h => h(o));
                break;
            case pe.PROGRESS:
                this.#u.forEach(h => h(o));
                break;
            case pe.ERROR:
                this.#l[b](o);
                break
            }
            delete this.#a[b], delete this.#l[b]
        })
    };
    #e = ({
        type: b,
        data: N
    }, o = [], h) => this.#t ? new Promise((z, C) => {
        const R = fv();
        this.#t && this.#t.postMessage({
            id: R,
            type: b,
            data: N
        }, o), this.#a[R] = z, this.#l[R] = C, h?.addEventListener("abort", () => {
            C(new DOMException(`Message # ${R} was aborted`, "AbortError"))
        }, {
            once: !0
        })
    }) : Promise.reject(ov);
    on(b, N) {
        b === "log" ? this.#n.push(N) : b === "progress" && this.#u.push(N)
    }
    off(b, N) {
        b === "log" ? this.#n = this.#n.filter(o => o !== N) : b === "progress" && (this.#u = this.#u.filter(o => o !== N))
    }
    load = ({
        classWorkerURL: b,
        ...N
    } = {}, {
        signal: o
    } = {}) => (this.#t || (this.#t = b ? new Worker(new URL(b,
        import.meta.url), {
        type: "module"
    }) : new Worker(new URL("/assets/worker-BAOIWoxA.js",
        import.meta.url), {
        type: "module"
    }), this.#i()), this.#e({
        type: pe.LOAD,
        data: N
    }, void 0, o));
    exec = (b, N = -1, {
        signal: o
    } = {}) => this.#e({
        type: pe.EXEC,
        data: {
            args: b,
            timeout: N
        }
    }, void 0, o);
    ffprobe = (b, N = -1, {
        signal: o
    } = {}) => this.#e({
        type: pe.FFPROBE,
        data: {
            args: b,
            timeout: N
        }
    }, void 0, o);
    terminate = () => {
        const b = Object.keys(this.#l);
        for (const N of b) this.#l[N](rv), delete this.#l[N], delete this.#a[N];
        this.#t && (this.#t.terminate(), this.#t = null, this.loaded = !1)
    };
    writeFile = (b, N, {
        signal: o
    } = {}) => {
        const h = [];
        return N instanceof Uint8Array && h.push(N.buffer), this.#e({
            type: pe.WRITE_FILE,
            data: {
                path: b,
                data: N
            }
        }, h, o)
    };
    mount = (b, N, o) => {
        const h = [];
        return this.#e({
            type: pe.MOUNT,
            data: {
                fsType: b,
                options: N,
                mountPoint: o
            }
        }, h)
    };
    unmount = b => {
        const N = [];
        return this.#e({
            type: pe.UNMOUNT,
            data: {
                mountPoint: b
            }
        }, N)
    };
    readFile = (b, N = "binary", {
        signal: o
    } = {}) => this.#e({
        type: pe.READ_FILE,
        data: {
            path: b,
            encoding: N
        }
    }, void 0, o);
    deleteFile = (b, {
        signal: N
    } = {}) => this.#e({
        type: pe.DELETE_FILE,
        data: {
            path: b
        }
    }, void 0, N);
    rename = (b, N, {
        signal: o
    } = {}) => this.#e({
        type: pe.RENAME,
        data: {
            oldPath: b,
            newPath: N
        }
    }, void 0, o);
    createDir = (b, {
        signal: N
    } = {}) => this.#e({
        type: pe.CREATE_DIR,
        data: {
            path: b
        }
    }, void 0, N);
    listDir = (b, {
        signal: N
    } = {}) => this.#e({
        type: pe.LIST_DIR,
        data: {
            path: b
        }
    }, void 0, N);
    deleteDir = (b, {
        signal: N
    } = {}) => this.#e({
        type: pe.DELETE_DIR,
        data: {
            path: b
        }
    }, void 0, N)
}
var $d;
(function (f) {
    f.MEMFS = "MEMFS", f.NODEFS = "NODEFS", f.NODERAWFS = "NODERAWFS", f.IDBFS = "IDBFS", f.WORKERFS = "WORKERFS", f.PROXYFS = "PROXYFS"
})($d || ($d = {}));
const mv = f => new Promise((b, N) => {
        const o = new FileReader;
        o.onload = () => {
            const {
                result: h
            } = o;
            h instanceof ArrayBuffer ? b(new Uint8Array(h)) : b(new Uint8Array)
        }, o.onerror = h => {
            N(Error(`File could not be read! Code=${h?.target?.error?.code||-1}`))
        }, o.readAsArrayBuffer(f)
    }),
    nm = async f => {
        let b;
        if (typeof f == "string") /data:_data\/([a-zA-Z]*);base64,([^"]*)/.test(f) ? b = atob(f.split(",")[1]).split("").map(N => N.charCodeAt(0)) : b = await (await fetch(f)).arrayBuffer();
        else if (f instanceof URL) b = await (await fetch(f)).arrayBuffer();
        else if (f instanceof File || f instanceof Blob) b = await mv(f);
        else return new Uint8Array;
        return new Uint8Array(b)
    }, hv = "/assets/ffmpeg-core-D7VZX-aa.js", vv = "/assets/ffmpeg-core-Cbz6om2n.wasm";
let ot = null;
async function gv(f) {
    ot?.loaded || (ot = new dv, await ot.load({
        coreURL: hv,
        wasmURL: vv
    }));
    let b = 30;
    const N = ({
        message: h
    }) => {
        const z = h.match(/,\s*(\d+(?:\.\d+)?)\s*(fps|tbr)/);
        z && (b = parseFloat(z[1]))
    };
    ot.on("log", N);
    const o = f.name.substring(f.name.lastIndexOf(".")) || ".mp4";
    await ot.writeFile("tmp" + o, await nm(f));
    try {
        await ot.exec(["-i", "tmp" + o])
    } catch {}
    return await ot.deleteFile("tmp" + o), ot.off("log", N), Math.round(b)
}

function yv({
    t: f,
    isVerified: b = !0,
    onAuthClick: N
}) {
    const [o, h] = L.useState(null), [z, C] = L.useState(null), [R, _] = L.useState(30), [S, q] = L.useState(!1), M = L.useRef(null), X = async K => {
        const ae = K.target.files?. [0];
        if (ae?.type.startsWith("video/")) {
            h(ae), C(null);
            try {
                C(await gv(ae))
            } catch {
                C(30)
            }
        }
    }, w = async () => {
        if (!(!o || !z || !ot)) {
            q(!0);
            try {
                const K = o.name.substring(o.name.lastIndexOf(".")) || ".mp4",
                    ae = (z / R).toFixed(4);
                await ot.writeFile("in" + K, await nm(o)), await ot.exec(["-itsscale", ae, "-i", "in" + K, "-c", "copy", "out" + K]);
                const J = await ot.readFile("out" + K),
                    ze = URL.createObjectURL(new Blob([J], {
                        type: o.type
                    }));
                Object.assign(document.createElement("a"), {
                    href: ze,
                    download: o.name.replace(/(\.[^.]+)$/, `_${R}fps$1`)
                }).click(), await ot.deleteFile("in" + K), await ot.deleteFile("out" + K)
            } catch {} finally {
                q(!1)
            }
        }
    }, V = () => {
        h(null), C(null), M.current && (M.current.value = "")
    };
    return c.jsxs("div", {
        className: "vc-section",
        children: [c.jsxs("div", {
            className: "section-title",
            children: [c.jsx(Kd, {
                size: 14
            }), " ", f("videoPatcher")]
        }), c.jsxs("div", {
            className: "vc-card",
            children: [!b && c.jsx("div", {
                className: "lock-overlay",
                onClick: N,
                children: c.jsx(Ct, {
                    size: 16
                })
            }), c.jsx("input", {
                ref: M,
                type: "file",
                accept: "video/*",
                onChange: X,
                style: {
                    display: "none"
                },
                disabled: !b
            }), o ? c.jsxs("div", {
                className: "vc-content",
                children: [c.jsxs("div", {
                    className: "vc-file",
                    children: [c.jsx(Kd, {
                        size: 14
                    }), c.jsx("span", {
                        className: "vc-filename",
                        children: o.name
                    }), c.jsx("button", {
                        className: "vc-remove",
                        onClick: V,
                        children: "×"
                    })]
                }), c.jsxs("div", {
                    className: "vc-fps-row",
                    children: [c.jsxs("div", {
                        className: "vc-fps-item",
                        children: [c.jsx("label", {
                            children: f("originalFps")
                        }), c.jsx("div", {
                            className: "vc-fps-value",
                            children: z || "..."
                        })]
                    }), c.jsx("div", {
                        className: "vc-fps-arrow",
                        children: "→"
                    }), c.jsxs("div", {
                        className: "vc-fps-item",
                        children: [c.jsx("label", {
                            children: f("targetFps")
                        }), c.jsx("input", {
                            type: "number",
                            value: R,
                            onChange: K => _(+K.target.value || 30),
                            min: 1,
                            max: z || 60
                        })]
                    })]
                }), c.jsxs("div", {
                    className: "vc-info",
                    children: ["Scale: ", z ? (z / R).toFixed(2) : "...", "x"]
                }), c.jsx("div", {
                    className: "vc-btn",
                    onClick: S ? void 0 : w,
                    children: S ? c.jsxs(c.Fragment, {
                        children: [c.jsx(Pu, {
                            size: 12,
                            className: "spin"
                        }), " ", f("processing")]
                    }) : c.jsxs(c.Fragment, {
                        children: [c.jsx(I1, {
                            size: 12
                        }), " ", f("patchVideo")]
                    })
                })]
            }) : c.jsxs("div", {
                className: "vc-dropzone",
                onClick: b ? () => M.current?.click() : void 0,
                children: [c.jsx(C0, {
                    size: 20
                }), c.jsx("span", {
                    children: f("selectVideo")
                })]
            })]
        })]
    })
}
const pv = [{
    name: "@editing_news",
    url: "https://t.me/editing_news"
}, {
    name: "@lexuof",
    url: "https://t.me/lexuof"
}];

function Sv({
    onClose: f,
    onCheck: b,
    t: N
}) {
    const [o, h] = L.useState(!1), [z, C] = L.useState(!1), [R, _] = L.useState(!1), S = async () => {
        if (o) return;
        h(!0), _(!1);
        const X = await b();
        h(!1), X ? (C(!0), setTimeout(f, 1200)) : _(!0)
    }, q = o ? Pu : z ? js : R ? Pd : w1, M = z ? "success" : R ? "error" : "";
    return c.jsx("div", {
        className: "modal-overlay",
        onClick: f,
        children: c.jsxs("div", {
            className: "auth-modal",
            onClick: X => X.stopPropagation(),
            children: [c.jsx("button", {
                className: "modal-close",
                onClick: f,
                children: c.jsx(Ds, {
                    size: 16
                })
            }), c.jsx("div", {
                className: `auth-icon ${M}`,
                children: c.jsx(q, {
                    size: 36,
                    className: o ? "auth-spin" : ""
                })
            }), c.jsx("h2", {
                className: "auth-title",
                children: N(z ? "authSuccess" : "subscriptionRequired")
            }), !z && c.jsxs(c.Fragment, {
                children: [c.jsx("p", {
                    className: "auth-desc",
                    children: N("subscriptionDesc")
                }), c.jsx("div", {
                    className: "auth-channels",
                    children: pv.map(X => c.jsx("button", {
                        className: "channel-btn",
                        onClick: () => chrome.tabs.create({
                            url: X.url
                        }),
                        children: X.name
                    }, X.name))
                })]
            }), R && c.jsx("p", {
                className: "auth-error",
                children: N("notSubscribedYet")
            }), !z && c.jsxs("button", {
                className: "auth-btn",
                onClick: S,
                children: [o ? c.jsx(Pu, {
                    size: 16,
                    className: "auth-spin"
                }) : c.jsx(js, {
                    size: 16
                }), N("checkSubscription")]
            })]
        })
    })
}

function bv({
    hasPartnerAccess: f,
    studioMethodMode: b,
    hqUpload: N,
    onToggle: o,
    isVerified: h,
    onAuthClick: z,
    dailyUsed: C,
    dailyLimit: R,
    usagePeriod: _,
    t: S
}) {
    const [q, M] = L.useState(!1), X = Math.max(0, R - C), w = C >= R, V = S(_ === "weekly" ? "weeklyRemaining" : "dailyRemaining"), K = S(_ === "weekly" ? "weeklyLimitReached" : "dailyLimitReached");
    return b === "off" ? c.jsxs("div", {
        className: "sm-card sm-dev",
        onClick: () => M(!q),
        children: [c.jsx("div", {
            className: "sm-glow sm-glow-purple"
        }), c.jsxs("div", {
            className: "sm-head",
            children: [c.jsx(S0, {
                size: 14,
                className: "sm-icon"
            }), c.jsx("span", {
                className: "sm-title",
                children: "STUDIO METHOD"
            }), c.jsx("span", {
                className: "sm-tag sm-tag-dev",
                children: S("studioTagDev")
            }), c.jsx(Iu, {
                size: 12,
                className: `sm-chevron ${q?"sm-chevron-open":""}`
            })]
        }), c.jsxs("div", {
            className: "sm-bar",
            children: [c.jsx("div", {
                className: "sm-bar-track",
                children: c.jsx("div", {
                    className: "sm-bar-fill",
                    style: {
                        width: "78%"
                    }
                })
            }), c.jsxs("span", {
                className: "sm-bar-pct",
                children: [78, "%"]
            })]
        }), q && c.jsxs("div", {
            className: "sm-expand",
            children: [c.jsx("p", {
                className: "sm-desc",
                children: S("studioMethodDesc")
            }), f && c.jsxs("div", {
                className: "sm-partner-note",
                children: [c.jsx(ti, {
                    size: 10
                }), c.jsx("span", {
                    children: S("studioPartnerNote")
                })]
            })]
        })]
    }) : b === "partners" ? c.jsxs("div", {
        className: "sm-card sm-live",
        children: [c.jsx("div", {
            className: "sm-glow sm-glow-green"
        }), c.jsxs("div", {
            className: "sm-head",
            onClick: () => M(!q),
            children: [c.jsx(As, {
                size: 14,
                className: "sm-icon sm-green"
            }), c.jsx("span", {
                className: "sm-title sm-green",
                children: "STUDIO METHOD"
            }), c.jsx("span", {
                className: "sm-tag sm-tag-live",
                children: "LIVE"
            }), c.jsx(Iu, {
                size: 12,
                className: `sm-chevron ${q?"sm-chevron-open":""}`
            })]
        }), c.jsxs("div", {
            className: "sm-toggle",
            style: {
                position: "relative",
                overflow: "hidden"
            },
            onClick: h ? void 0 : z,
            children: [!h && c.jsx("div", {
                className: "lock-overlay",
                onClick: z,
                children: c.jsx(Ct, {
                    size: 14
                })
            }), c.jsxs("div", {
                className: "sm-toggle-info",
                children: [c.jsx("span", {
                    className: "sm-toggle-name",
                    children: S("hqUpload")
                }), c.jsx("span", {
                    className: "sm-toggle-hint",
                    children: S("hqUploadDesc")
                })]
            }), f ? c.jsx(Ra, {
                active: N,
                onClick: o,
                mini: !0
            }) : c.jsx(Ct, {
                size: 12,
                className: "lock-icon-inline"
            })]
        }), !f && c.jsxs("div", {
            className: "sm-lock-msg",
            children: [c.jsx(Ct, {
                size: 10
            }), c.jsx("span", {
                children: S("studioPartnerOnly")
            })]
        }), h && f && c.jsxs("div", {
            className: `sm-usage ${w?"sm-usage-full":""}`,
            children: [c.jsx("div", {
                className: "sm-usage-dots",
                children: Array.from({
                    length: R
                }, (ae, J) => c.jsx("div", {
                    className: `sm-dot ${J<C?"sm-dot-used":""}`
                }, J))
            }), c.jsx("span", {
                children: w ? K : `${X} ${V}`
            })]
        }), q && c.jsx("div", {
            className: "sm-expand",
            children: c.jsx("p", {
                className: "sm-desc",
                children: S("studioMethodLiveDesc")
            })
        })]
    }) : c.jsxs("div", {
        className: "sm-card sm-live",
        children: [c.jsx("div", {
            className: "sm-glow sm-glow-green"
        }), c.jsxs("div", {
            className: "sm-head",
            onClick: () => M(!q),
            children: [c.jsx(As, {
                size: 14,
                className: "sm-icon sm-green"
            }), c.jsx("span", {
                className: "sm-title sm-green",
                children: "STUDIO METHOD"
            }), c.jsx("span", {
                className: "sm-tag sm-tag-live",
                children: "LIVE"
            }), c.jsx(Iu, {
                size: 12,
                className: `sm-chevron ${q?"sm-chevron-open":""}`
            })]
        }), c.jsxs("div", {
            className: "sm-toggle",
            style: {
                position: "relative",
                overflow: "hidden"
            },
            onClick: h ? void 0 : z,
            children: [!h && c.jsx("div", {
                className: "lock-overlay",
                onClick: z,
                children: c.jsx(Ct, {
                    size: 14
                })
            }), c.jsxs("div", {
                className: "sm-toggle-info",
                children: [c.jsx("span", {
                    className: "sm-toggle-name",
                    children: S("hqUpload")
                }), c.jsx("span", {
                    className: "sm-toggle-hint",
                    children: S("studioMethodAllDesc")
                })]
            }), c.jsx(Ra, {
                active: N,
                onClick: o,
                mini: !0
            })]
        }), h && c.jsxs("div", {
            className: `sm-usage ${w?"sm-usage-full":""}`,
            children: [c.jsx("div", {
                className: "sm-usage-dots",
                children: Array.from({
                    length: R
                }, (ae, J) => c.jsx("div", {
                    className: `sm-dot ${J<C?"sm-dot-used":""}`
                }, J))
            }), c.jsx("span", {
                children: w ? K : `${X} ${V}`
            })]
        }), q && c.jsx("div", {
            className: "sm-expand",
            children: c.jsx("p", {
                className: "sm-desc",
                children: S("studioMethodLiveDesc")
            })
        })]
    })
}

function Nv() {
    const [f, b] = L.useState(() => {
        const z = localStorage.getItem("promo_end");
        if (z) {
            const R = parseInt(z) - Date.now();
            if (R > 0) return R
        }
        const C = (2 * 3600 + Math.floor(Math.random() * 3 * 3600)) * 1e3;
        return localStorage.setItem("promo_end", String(Date.now() + C)), C
    });
    L.useEffect(() => {
        const z = setInterval(() => {
            b(C => {
                const R = C - 1e3;
                if (R <= 0) {
                    const _ = (7200 + Math.floor(Math.random() * 3 * 3600)) * 1e3;
                    return localStorage.setItem("promo_end", String(Date.now() + _)), _
                }
                return R
            })
        }, 1e3);
        return () => clearInterval(z)
    }, []);
    const N = Math.floor(f / 36e5),
        o = Math.floor(f % 36e5 / 6e4),
        h = Math.floor(f % 6e4 / 1e3);
    return `${N}:${String(o).padStart(2,"0")}:${String(h).padStart(2,"0")}`
}

function Ev({
    hasPartnerAccess: f,
    canDisableWatermark: b,
    isVerified: N,
    addSignature: o,
    enhancedStats: h,
    originalDownload: z,
    onToggleSignature: C,
    onToggleEnhancedStats: R,
    onToggleOriginalDownload: _,
    onLockClick: S,
    onAuthClick: q,
    t: M
}) {
    const X = Nv(),
        w = !N || !f,
        V = N ? S : q,
        K = !N || !b,
        ae = K ? !0 : o,
        J = () => {
            chrome.tabs.create({
                url: "https://t.me/editingnews_bot"
            })
        },
        ze = () => {
            chrome.tabs.create({
                url: "https://t.me/manager_en"
            })
        };
    return c.jsxs("div", {
        className: "pricing-section",
        children: [c.jsxs("div", {
            className: "pricing-head",
            children: [c.jsx(ti, {
                size: 14,
                className: "crown-icon"
            }), c.jsx("span", {
                className: "pricing-title",
                children: M("partnershipFeatures")
            }), c.jsxs("div", {
                className: "pricing-info-wrap",
                children: [c.jsx("div", {
                    className: "pricing-info-btn",
                    children: "i"
                }), c.jsxs("div", {
                    className: "pricing-tooltip",
                    children: [c.jsx("p", {
                        children: M("premiumBenefit1")
                    }), c.jsx("p", {
                        children: M("premiumBenefit2")
                    }), c.jsx("p", {
                        children: M("premiumBenefit3")
                    }), c.jsx("p", {
                        children: M("premiumBenefit4")
                    })]
                })]
            })]
        }), c.jsxs("div", {
            className: "pricing-urgency",
            children: [c.jsx(As, {
                size: 12
            }), c.jsxs("span", {
                children: [M("saleEnds"), " ", X]
            })]
        }), c.jsxs("div", {
            className: "pricing-cards",
            children: [c.jsxs("div", {
                className: "pricing-card",
                children: [c.jsx("div", {
                    className: "pricing-discount-tag",
                    children: "-50%"
                }), c.jsx("div", {
                    className: "pricing-period",
                    children: M("perMonth")
                }), c.jsxs("div", {
                    className: "pricing-row",
                    children: [c.jsx("span", {
                        className: "pricing-old",
                        children: "$29.99"
                    }), c.jsx("span", {
                        className: "pricing-new",
                        children: "$14.99"
                    })]
                }), c.jsxs("div", {
                    className: "pricing-row",
                    children: [c.jsx("span", {
                        className: "pricing-old",
                        children: "1 199₽"
                    }), c.jsx("span", {
                        className: "pricing-new",
                        children: "599₽"
                    })]
                }), c.jsxs("div", {
                    className: "pricing-perday",
                    children: ["~$0.50/", M("day")]
                })]
            }), c.jsxs("div", {
                className: "pricing-card pricing-best",
                children: [c.jsx("div", {
                    className: "pricing-best-tag",
                    children: M("popular")
                }), c.jsxs("div", {
                    className: "pricing-save-tag",
                    children: [M("save"), " 44%"]
                }), c.jsx("div", {
                    className: "pricing-period",
                    children: M("per3Months")
                }), c.jsxs("div", {
                    className: "pricing-row",
                    children: [c.jsx("span", {
                        className: "pricing-old",
                        children: "$44.99"
                    }), c.jsx("span", {
                        className: "pricing-new",
                        children: "$24.99"
                    })]
                }), c.jsxs("div", {
                    className: "pricing-row",
                    children: [c.jsx("span", {
                        className: "pricing-old",
                        children: "2 999₽"
                    }), c.jsx("span", {
                        className: "pricing-new",
                        children: "1 499₽"
                    })]
                }), c.jsxs("div", {
                    className: "pricing-perday",
                    children: ["~$8.33/", M("mo"), " · ~500₽/", M("mo")]
                })]
            })]
        }), c.jsxs("div", {
            className: "pricing-actions",
            children: [c.jsxs("button", {
                className: "pricing-btn pricing-btn-apply",
                onClick: ze,
                children: [c.jsx(Ms, {
                    size: 13
                }), M("applyPartnership")]
            }), c.jsx("span", {
                className: "pricing-or",
                children: M("or")
            }), c.jsxs("button", {
                className: "pricing-btn pricing-btn-buy",
                onClick: J,
                children: [c.jsx(x0, {
                    size: 13
                }), M("buyInBot")]
            })]
        }), c.jsxs("div", {
            className: "partnership-toggles",
            children: [c.jsxs("div", {
                className: "partnership-item",
                style: {
                    position: "relative",
                    overflow: "hidden"
                },
                onClick: K ? V : void 0,
                children: [K && c.jsx("div", {
                    className: "lock-overlay",
                    onClick: V,
                    children: c.jsx(Ct, {
                        size: 16
                    })
                }), c.jsx("div", {
                    className: "partnership-icon",
                    children: c.jsx(R0, {
                        size: 16
                    })
                }), c.jsxs("div", {
                    className: "partnership-content",
                    children: [c.jsx("h4", {
                        children: M("addSignature")
                    }), c.jsx("p", {
                        children: M("addSignatureDesc")
                    })]
                }), c.jsx(Ra, {
                    active: ae,
                    onClick: K ? void 0 : C,
                    mini: !0
                })]
            }), c.jsxs("div", {
                className: "partnership-item",
                style: {
                    position: "relative",
                    overflow: "hidden"
                },
                onClick: w ? V : void 0,
                children: [w && c.jsx("div", {
                    className: "lock-overlay",
                    onClick: V,
                    children: c.jsx(Ct, {
                        size: 16
                    })
                }), c.jsx("div", {
                    className: "partnership-icon",
                    children: c.jsx(Id, {
                        size: 16
                    })
                }), c.jsxs("div", {
                    className: "partnership-content",
                    children: [c.jsx("h4", {
                        children: M("enhancedStats")
                    }), c.jsx("p", {
                        children: M("enhancedStatsDesc")
                    })]
                }), c.jsx(Ra, {
                    active: h,
                    onClick: w ? void 0 : R,
                    mini: !0
                })]
            }), c.jsxs("div", {
                className: "partnership-item",
                style: {
                    position: "relative",
                    overflow: "hidden"
                },
                onClick: w ? V : void 0,
                children: [w && c.jsx("div", {
                    className: "lock-overlay",
                    onClick: V,
                    children: c.jsx(Ct, {
                        size: 16
                    })
                }), c.jsx("div", {
                    className: "partnership-icon",
                    children: c.jsx(j0, {
                        size: 16
                    })
                }), c.jsxs("div", {
                    className: "partnership-content",
                    children: [c.jsx("h4", {
                        children: M("originalDownload")
                    }), c.jsx("p", {
                        children: M("originalDownloadDesc")
                    })]
                }), c.jsx(Ra, {
                    active: z,
                    onClick: w ? void 0 : _,
                    mini: !0
                })]
            })]
        })]
    })
}

function Tv(f) {
    return {
        panelTitle: f("repostPanelTitle"),
        preparing: f("repostPreparing"),
        paused: f("repostPaused"),
        resuming: f("repostResuming"),
        btnPause: f("repostBtnPause"),
        btnResume: f("repostBtnResume"),
        btnDownload: f("repostBtnDownload"),
        waiting: f("repostWaiting"),
        listing: f("repostListing"),
        pageRemoving: f("repostPageRemoving"),
        done: f("repostDone"),
        none: f("repostNone"),
        errorNoAccount: f("repostErrorNoAccount"),
        errorNotLoggedIn: f("repostErrorNotLoggedIn"),
        errorRemove: f("repostErrorRemove"),
        close: f("repostClose"),
        statsPages: f("repostStatsPages"),
        statsRemoved: f("repostStatsRemoved"),
        statsListed: f("repostStatsListed"),
        statsFailed: f("repostStatsFailed"),
        stoppedFailures: f("repostStoppedFailures"),
        betweenPages: f("repostBetweenPages")
    }
}

function xv({
    t: f,
    isVerified: b = !0,
    onAuthClick: N
}) {
    const [o, h] = L.useState(!1), [z, C] = L.useState(!1), [R, _] = L.useState(""), [S, q] = L.useState("range"), [M, X] = L.useState(1), [w, V] = L.useState(3), [K, ae] = L.useState("1, 3, 5"), [J, ze] = L.useState(5), [F, Re] = L.useState("json"), W = L.useCallback(() => {
        o || et.get(["repostRemoverConfig"]).then(O => {
            const U = O.repostRemoverConfig;
            U && (_(U.keywordsFilter || ""), C(!!U.keywordsFilter), q(U.requestIntervalMode || "range"), X(U.requestIntervalRange?.min ?? 1), V(U.requestIntervalRange?.max ?? 3), ae(U.requestIntervalSet?.join(", ") || "1, 3, 5"), ze(U.pagePauseSeconds ?? 5), Re(U.exportFileType || "json"))
        }), h(O => !O)
    }, [o]), Q = L.useCallback(() => {
        const O = K.split(",").map(ne => parseInt(ne.trim(), 10)).filter(ne => !isNaN(ne) && ne >= 0),
            U = {
                keywordsFilter: z ? R : "",
                requestIntervalMode: S,
                requestIntervalRange: {
                    min: Math.max(1, M),
                    max: Math.max(M, w)
                },
                requestIntervalSet: O.length ? O : [1, 3, 5],
                exportFileType: F,
                pagePauseSeconds: Math.max(0, J)
            };
        et.set({
            repostRemoverConfig: U
        }), chrome.runtime.sendMessage({
            action: "startRepostRemoval",
            config: {
                ...U,
                i18n: Tv(f)
            }
        }), window.close()
    }, [z, R, S, M, w, K, J, F, f]);
    return c.jsx("div", {
        className: "rr-section",
        children: c.jsxs("div", {
            className: "rr-card",
            children: [!b && c.jsx("div", {
                className: "lock-overlay",
                onClick: N,
                children: c.jsx(Ct, {
                    size: 16
                })
            }), c.jsxs("div", {
                className: "rr-header",
                onClick: b ? W : void 0,
                children: [c.jsx("div", {
                    className: "rr-header-icon",
                    children: c.jsx(y0, {
                        size: 16
                    })
                }), c.jsxs("div", {
                    className: "rr-header-content",
                    children: [c.jsx("div", {
                        className: "rr-header-title",
                        children: f("repostRemover")
                    }), c.jsx("div", {
                        className: "rr-header-desc",
                        children: f("repostRemoverDesc")
                    })]
                }), c.jsx(Iu, {
                    size: 14,
                    className: `rr-chevron ${o?"rr-chevron-open":""}`
                })]
            }), o && c.jsxs("div", {
                className: "rr-body",
                children: [c.jsxs("div", {
                    className: "rr-row",
                    children: [c.jsxs("label", {
                        className: "rr-checkbox",
                        children: [c.jsx("input", {
                            type: "checkbox",
                            checked: z,
                            onChange: O => C(O.target.checked)
                        }), c.jsx("span", {
                            children: f("repostFilterKeywords")
                        })]
                    }), z && c.jsx("input", {
                        className: "rr-input",
                        type: "text",
                        placeholder: f("repostKeywordsPlaceholder"),
                        value: R,
                        onChange: O => _(O.target.value)
                    })]
                }), c.jsxs("div", {
                    className: "rr-row",
                    children: [c.jsx("div", {
                        className: "rr-label",
                        children: f("repostInterval")
                    }), c.jsxs("select", {
                        className: "rr-select",
                        value: S,
                        onChange: O => q(O.target.value),
                        children: [c.jsx("option", {
                            value: "range",
                            children: f("repostIntervalRange")
                        }), c.jsx("option", {
                            value: "set",
                            children: f("repostIntervalSet")
                        })]
                    }), S === "range" ? c.jsxs("div", {
                        className: "rr-range-row",
                        children: [c.jsx("input", {
                            className: "rr-input rr-input-small",
                            type: "number",
                            min: 1,
                            max: 10,
                            value: M,
                            onChange: O => {
                                const U = Math.max(1, Math.min(10, parseInt(O.target.value) || 1));
                                X(U), U > w && V(U)
                            }
                        }), c.jsx("span", {
                            className: "rr-range-sep",
                            children: "–"
                        }), c.jsx("input", {
                            className: "rr-input rr-input-small",
                            type: "number",
                            min: 1,
                            max: 10,
                            value: w,
                            onChange: O => {
                                const U = Math.max(1, Math.min(10, parseInt(O.target.value) || 3));
                                V(U), U < M && X(U)
                            }
                        }), c.jsx("span", {
                            className: "rr-range-unit",
                            children: "s"
                        })]
                    }) : c.jsx("input", {
                        className: "rr-input",
                        type: "text",
                        placeholder: "1, 3, 5",
                        value: K,
                        onChange: O => ae(O.target.value)
                    })]
                }), c.jsxs("div", {
                    className: "rr-row rr-inline-row",
                    children: [c.jsx("div", {
                        className: "rr-label",
                        children: f("repostPagePause")
                    }), c.jsx("input", {
                        className: "rr-input rr-input-small",
                        type: "number",
                        min: 0,
                        max: 120,
                        value: J,
                        onChange: O => ze(Math.max(0, parseInt(O.target.value) || 0))
                    })]
                }), c.jsxs("div", {
                    className: "rr-row rr-inline-row",
                    children: [c.jsx("div", {
                        className: "rr-label",
                        children: f("repostReport")
                    }), c.jsxs("select", {
                        className: "rr-select",
                        value: F,
                        onChange: O => Re(O.target.value),
                        children: [c.jsx("option", {
                            value: "json",
                            children: "JSON"
                        }), c.jsx("option", {
                            value: "csv",
                            children: "CSV"
                        })]
                    })]
                }), c.jsxs("div", {
                    className: "rr-start",
                    onClick: Q,
                    children: [c.jsx(v0, {
                        size: 12
                    }), " ", f("repostStart")]
                })]
            })]
        })
    })
}
const Wu = {
        addSignature: !0,
        fps60: !0,
        promoVideos: !0,
        authorStats: !0,
        videoStats: !0,
        studioDarkMode: !0,
        enhancedStats: !1,
        hqUpload: !1,
        originalDownload: !1
    },
    An = {
        addSignature: !1,
        fps60: !1,
        promoVideos: !1,
        authorStats: !1,
        videoStats: !1,
        studioDarkMode: !1,
        enhancedStats: !1,
        hqUpload: !1,
        originalDownload: !1
    };

function $u(f) {
    return Array.isArray(f) ? f.map(b => b === "editing_partnership" ? "partner" : b === "editing_plus" || b === "editing_premium" ? "premium" : b === "owner" || b === "editing" || b === "partner" || b === "premium" ? b : null).filter(b => b !== null) : []
}

function _n(f, b, N, o) {
    const h = {
        ...f
    };
    h.fps60 && h.hqUpload && (h.hqUpload = !1);
    const z = N || b && (!h.hqUpload || o);
    return z || (h.addSignature = !0), {
        featureSettings: h,
        canDisableWatermark: z
    }
}

function zv() {
    const {
        t: f,
        language: b,
        toggleLanguage: N,
        isChanging: o
    } = w0(), [h, z] = L.useState({
        isLoggedIn: !1,
        session: "",
        userId: "",
        username: "",
        firstName: "",
        avatar: "",
        isSubscribed: !1,
        isPartner: !1,
        isPremium: !1,
        badges: [],
        studioMethodMode: "off",
        canDisableWatermark: !1,
        allowPartnershipNoWatermark: !1,
        dailyUsed: 0,
        dailyLimit: 1,
        usagePeriod: "weekly",
        loading: !0,
        features: An
    }), [C, R] = L.useState(!1), [_, S] = L.useState(!1), [q, M] = L.useState(null), [X, w] = L.useState(!1), [V, K] = L.useState("home"), ae = L.useCallback(W => {
        M(W), setTimeout(() => M(null), 3e3)
    }, []);
    L.useEffect(() => {
        async function W() {
            const Q = await et.get(["session", "userId", "username", "firstName", "avatar", "isSubscribed", "isPartner", "isPremium", "badges", "studioMethodMode", "canDisableWatermark", "allowPartnershipNoWatermark", "featureSettings", "dailyUsed", "dailyLimit", "usagePeriod"]),
                O = !!Q.session,
                U = Q.isSubscribed || !1,
                ne = Q.isPartner || !1,
                Ue = Q.isPremium || !1,
                je = Q.allowPartnershipNoWatermark || !1,
                Me = $u(Q.badges || []),
                Ie = U ? _n(Q.featureSettings || Wu, ne, Ue, je) : {
                    featureSettings: An,
                    canDisableWatermark: !1
                };
            z({
                isLoggedIn: O,
                session: Q.session || "",
                userId: Q.userId || "",
                username: Q.username || "",
                firstName: Q.firstName || "",
                avatar: Q.avatar || "",
                isSubscribed: U,
                isPartner: ne,
                isPremium: Ue,
                badges: Me,
                studioMethodMode: Q.studioMethodMode || "off",
                canDisableWatermark: Ie.canDisableWatermark,
                allowPartnershipNoWatermark: je,
                dailyUsed: Q.dailyUsed ?? 0,
                dailyLimit: Q.dailyLimit ?? 1,
                usagePeriod: Q.usagePeriod || "weekly",
                loading: !1,
                features: Ie.featureSettings
            })
        }
        return W(), et.onChange(async Q => {
            if (Q.session || Q.isSubscribed || Q.isPartner || Q.isPremium || Q.badges || Q.featureSettings || Q.studioMethodMode || Q.canDisableWatermark || Q.allowPartnershipNoWatermark) {
                const O = await et.get(["session", "userId", "username", "firstName", "avatar", "isSubscribed", "isPartner", "isPremium", "badges", "studioMethodMode", "canDisableWatermark", "allowPartnershipNoWatermark", "featureSettings"]),
                    U = !!O.session,
                    ne = O.isSubscribed ?? !1,
                    Ue = O.isPartner ?? !1,
                    je = O.isPremium ?? !1,
                    Me = O.allowPartnershipNoWatermark ?? !1,
                    Ie = $u(O.badges ?? []),
                    Ze = ne ? _n(O.featureSettings || Wu, Ue, je, Me) : {
                        featureSettings: An,
                        canDisableWatermark: !1
                    };
                z(De => ({
                    ...De,
                    isLoggedIn: U,
                    session: O.session || De.session,
                    userId: O.userId || De.userId,
                    username: O.username || De.username,
                    firstName: O.firstName || De.firstName,
                    avatar: O.avatar || De.avatar,
                    isSubscribed: ne,
                    isPartner: Ue,
                    isPremium: je,
                    badges: Ie,
                    studioMethodMode: O.studioMethodMode ?? De.studioMethodMode,
                    canDisableWatermark: Ze.canDisableWatermark,
                    allowPartnershipNoWatermark: Me,
                    features: Ze.featureSettings
                }))
            }
        })
    }, []), L.useEffect(() => {
        let W = !1;
        async function Q() {
            if (!(!h.session || W)) {
                W = !0;
                try {
                    const U = await Fu.userCheck(h.session),
                        ne = U.user.avatar || "",
                        Ue = await et.get(["featureSettings"]),
                        je = $u(U.badges || []),
                        Me = U.isPremium ?? !1,
                        Ie = U.allowPartnershipNoWatermark ?? !1,
                        Ze = U.subscribed ? _n(Ue.featureSettings || Wu, U.isPartner, Me, Ie) : {
                            featureSettings: An,
                            canDisableWatermark: !1
                        };
                    await et.set({
                        username: U.user.username || "",
                        firstName: U.user.firstName || "",
                        ...ne ? {
                            avatar: ne
                        } : {},
                        isSubscribed: U.subscribed,
                        isPartner: U.isPartner,
                        isPremium: Me,
                        badges: je,
                        studioMethodMode: U.studioMethodMode,
                        canDisableWatermark: Ze.canDisableWatermark,
                        allowPartnershipNoWatermark: Ie,
                        featureSettings: Ze.featureSettings,
                        dailyUsed: U.dailyUsed ?? 0,
                        dailyLimit: U.dailyLimit ?? 1,
                        usagePeriod: U.usagePeriod || "weekly"
                    }), z(De => ({
                        ...De,
                        username: U.user.username || "",
                        firstName: U.user.firstName || "",
                        avatar: ne || De.avatar,
                        isSubscribed: U.subscribed,
                        isPartner: U.isPartner,
                        isPremium: Me,
                        badges: je,
                        studioMethodMode: U.studioMethodMode,
                        canDisableWatermark: Ze.canDisableWatermark,
                        allowPartnershipNoWatermark: Ie,
                        dailyUsed: U.dailyUsed ?? De.dailyUsed,
                        dailyLimit: U.dailyLimit ?? De.dailyLimit,
                        usagePeriod: U.usagePeriod || De.usagePeriod,
                        features: Ze.featureSettings
                    }))
                } catch (U) {
                    const ne = U?.message || "";
                    (ne === "HTTP_401" || ne === "INVALID_SESSION") && (await et.clear(), z(Ue => ({
                        ...Ue,
                        isLoggedIn: !1,
                        session: "",
                        features: An
                    })))
                } finally {
                    W = !1
                }
            }
        }!h.loading && h.session && Q();
        const O = () => {
            h.session && Q()
        };
        return window.addEventListener("focus", O), () => window.removeEventListener("focus", O)
    }, [h.session, h.loading]), L.useEffect(() => {
        const W = document.querySelector(".container");
        W && (W.scrollTop = 0)
    }, [V]);
    const J = L.useCallback(W => {
            if (!h.isLoggedIn) {
                R(!0);
                return
            }
            if (!h.isSubscribed) {
                S(!0);
                return
            }
            if (W === "addSignature" && !h.canDisableWatermark) {
                ae(f("notPartnerToast"));
                return
            }
            if (W === "enhancedStats" && !(h.isPartner || h.isPremium)) {
                ae(f("notPartnerToast"));
                return
            }
            if (W === "originalDownload" && !(h.isPartner || h.isPremium)) {
                ae(f("notPartnerToast"));
                return
            }
            z(Q => {
                const O = !Q.features[W],
                    U = {
                        ...Q.features,
                        [W]: O
                    };
                O && (W === "hqUpload" && U.fps60 && (U.fps60 = !1, ae(f("fpsDisabledByHq"))), W === "fps60" && U.hqUpload && (U.hqUpload = !1, ae(f("hqDisabledByFps"))));
                const ne = _n(U, Q.isPartner, Q.isPremium, Q.allowPartnershipNoWatermark);
                return et.set({
                    featureSettings: ne.featureSettings,
                    canDisableWatermark: ne.canDisableWatermark
                }), {
                    ...Q,
                    features: ne.featureSettings,
                    canDisableWatermark: ne.canDisableWatermark
                }
            })
        }, [h.isLoggedIn, h.isSubscribed, h.isPartner, h.isPremium, h.canDisableWatermark, ae, f]),
        ze = L.useCallback(async () => {
            if (h.session) try {
                await Fu.logout(h.session)
            } catch {}
            await et.clear(), window.location.reload()
        }, [h.session]),
        F = L.useCallback(() => {
            h.isLoggedIn ? h.isSubscribed || S(!0) : R(!0)
        }, [h.isLoggedIn, h.isSubscribed]),
        Re = L.useCallback(async () => {
            if (!h.session) return !1;
            try {
                const W = await Fu.userCheck(h.session);
                if (W.subscribed) {
                    const Q = await et.get(["featureSettings"]),
                        O = $u(W.badges || []),
                        U = W.isPremium ?? !1,
                        ne = W.allowPartnershipNoWatermark ?? !1,
                        Ue = _n(Q.featureSettings || Wu, W.isPartner, U, ne);
                    return await et.set({
                        isSubscribed: !0,
                        isPartner: W.isPartner,
                        isPremium: U,
                        badges: O,
                        studioMethodMode: W.studioMethodMode,
                        canDisableWatermark: Ue.canDisableWatermark,
                        allowPartnershipNoWatermark: ne,
                        featureSettings: Ue.featureSettings,
                        dailyUsed: W.dailyUsed ?? 0,
                        dailyLimit: W.dailyLimit ?? 1,
                        usagePeriod: W.usagePeriod || "weekly"
                    }), z(je => ({
                        ...je,
                        isSubscribed: !0,
                        isPartner: W.isPartner,
                        isPremium: U,
                        badges: O,
                        studioMethodMode: W.studioMethodMode,
                        canDisableWatermark: Ue.canDisableWatermark,
                        allowPartnershipNoWatermark: ne,
                        dailyUsed: W.dailyUsed ?? je.dailyUsed,
                        dailyLimit: W.dailyLimit ?? je.dailyLimit,
                        usagePeriod: W.usagePeriod || je.usagePeriod,
                        features: Ue.featureSettings
                    })), !0
                }
                return !1
            } catch {
                return !1
            }
        }, [h.session]);
    return h.loading ? null : c.jsxs("div", {
        className: `app theme-dark ${o?"lang-changing":""}`,
        children: [c.jsx("div", {
            className: "particles",
            children: [...Array(14)].map((W, Q) => {
                const O = (Q * 7 + 13) % 100,
                    U = (Q * 23 + 11) % 88 + 6,
                    ne = 8 + O / 100 * 88,
                    Ue = O % 3 === 0 ? "star-large" : O % 3 === 1 ? "star-medium" : "",
                    je = 5 + O % 50 / 10,
                    Me = Q * .9 % 12;
                return c.jsx("div", {
                    className: `particle ${Ue}`,
                    style: {
                        left: `${U}%`,
                        top: `${ne}%`,
                        animationDelay: `${Me}s`,
                        animationDuration: `${je}s`
                    }
                }, Q)
            })
        }), c.jsxs("div", {
            className: "container",
            children: [c.jsx($0, {
                state: h,
                language: b,
                onLanguageToggle: N,
                onProfileClick: () => K("profile"),
                onAuthClick: () => R(!0),
                t: f
            }), V === "home" && c.jsxs("div", {
                className: "tab-content",
                children: [c.jsxs("div", {
                    className: "header-title",
                    children: [c.jsx("div", {
                        className: "logo",
                        children: "TikTok Enhancer"
                    }), c.jsx("div", {
                        className: "subtitle",
                        children: f("subtitle")
                    })]
                }), c.jsx(bv, {
                    hasPartnerAccess: h.isPartner || h.isPremium,
                    studioMethodMode: h.studioMethodMode,
                    hqUpload: h.features.hqUpload,
                    onToggle: () => J("hqUpload"),
                    isVerified: h.isLoggedIn && h.isSubscribed,
                    onAuthClick: F,
                    dailyUsed: h.dailyUsed,
                    dailyLimit: h.dailyLimit,
                    usagePeriod: h.usagePeriod,
                    t: f
                }), c.jsx(Ev, {
                    hasPartnerAccess: h.isPartner || h.isPremium,
                    canDisableWatermark: h.canDisableWatermark,
                    isVerified: h.isLoggedIn && h.isSubscribed,
                    addSignature: h.features.addSignature,
                    enhancedStats: h.features.enhancedStats,
                    originalDownload: h.features.originalDownload,
                    onToggleSignature: () => J("addSignature"),
                    onToggleEnhancedStats: () => J("enhancedStats"),
                    onToggleOriginalDownload: () => J("originalDownload"),
                    onLockClick: () => ae(f("notPartnerToast")),
                    onAuthClick: F,
                    t: f
                })]
            }), V === "vpn" && c.jsx("div", {
                className: "tab-content",
                children: c.jsx(av, {
                    t: f
                })
            }), V === "settings" && c.jsx("div", {
                className: "tab-content",
                children: c.jsx(I0, {
                    t: f,
                    features: h.features,
                    onToggle: J,
                    isVerified: h.isLoggedIn && h.isSubscribed,
                    onAuthClick: F
                })
            }), V === "tools" && c.jsxs("div", {
                className: "tab-content",
                children: [c.jsx(yv, {
                    t: f,
                    isVerified: h.isLoggedIn && h.isSubscribed,
                    onAuthClick: F
                }), c.jsxs("div", {
                    className: "settings-section",
                    children: [c.jsxs("div", {
                        className: "setting-item",
                        style: {
                            cursor: "pointer",
                            position: "relative",
                            overflow: "hidden"
                        },
                        onClick: h.isLoggedIn && h.isSubscribed ? async () => {
                            if (!X) {
                                w(!0);
                                try {
                                    const W = await chrome.cookies.remove({
                                        url: "https://www.tiktok.com",
                                        name: "ttwid"
                                    });
                                    ae(f(W ? "cookieCleared" : "cookieNotFound"))
                                } catch {
                                    ae(f("cookieNotFound"))
                                } finally {
                                    w(!1)
                                }
                            }
                        } : F,
                        children: [!(h.isLoggedIn && h.isSubscribed) && c.jsx("div", {
                            className: "lock-overlay",
                            onClick: F,
                            children: c.jsx(Ct, {
                                size: 16
                            })
                        }), c.jsx("div", {
                            className: "setting-icon",
                            children: c.jsxs("svg", {
                                width: "16",
                                height: "16",
                                viewBox: "0 0 24 24",
                                fill: "none",
                                stroke: "currentColor",
                                strokeWidth: "2",
                                strokeLinecap: "round",
                                strokeLinejoin: "round",
                                children: [c.jsx("circle", {
                                    cx: "12",
                                    cy: "12",
                                    r: "10"
                                }), c.jsx("path", {
                                    d: "m4.9 4.9 14.2 14.2"
                                })]
                            })
                        }), c.jsxs("div", {
                            className: "setting-content",
                            children: [c.jsx("h4", {
                                children: f("clearCookies")
                            }), c.jsx("p", {
                                children: f("clearCookiesDesc")
                            })]
                        })]
                    }), c.jsx(xv, {
                        t: f,
                        isVerified: h.isLoggedIn && h.isSubscribed,
                        onAuthClick: F
                    })]
                })]
            }), V === "profile" && c.jsx("div", {
                className: "tab-content",
                children: c.jsx(sv, {
                    state: h,
                    onLogout: ze,
                    onAuthClick: () => R(!0),
                    version: D1.version,
                    t: f
                })
            })]
        }), c.jsx(lv, {
            activeTab: V,
            onTabChange: K,
            t: f
        }), C && c.jsx(J0, {
            onClose: () => R(!1),
            isLoggedIn: h.isLoggedIn,
            t: f
        }), _ && c.jsx(Sv, {
            onClose: () => S(!1),
            onCheck: Re,
            t: f
        }), q && c.jsx("div", {
            className: "toast-notification",
            children: c.jsx("span", {
                children: q
            })
        }), c.jsx(P0, {})]
    })
}
L1.createRoot(document.getElementById("root")).render(c.jsx(L.StrictMode, {
    children: c.jsx(zv, {})
}));
```


ffmpeg-core.js:

```
var createFFmpegCore = (() => {
  var _scriptDir = import.meta.url;
  return async function (createFFmpegCore = {}) {
    var Module = typeof createFFmpegCore != "undefined" ? createFFmpegCore : {};
    var readyPromiseResolve;
    var readyPromiseReject;
    Module.ready = new Promise((resolve, reject) => {
      readyPromiseResolve = resolve;
      readyPromiseReject = reject;
    });
    const SIZE_I32 = Uint32Array.BYTES_PER_ELEMENT;
    const DEFAULT_ARGS = ["./ffmpeg", "-nostdin", "-y"];
    Module.NULL = 0;
    Module.SIZE_I32 = SIZE_I32;
    Module.DEFAULT_ARGS = DEFAULT_ARGS;
    Module.ret = -1;
    Module.timeout = -1;
    Module.logger = () => {};
    Module.progress = () => {};
    function stringToPtr(str) {
      const len = Module.lengthBytesUTF8(str) + 1;
      const ptr = Module._malloc(len);
      Module.stringToUTF8(str, ptr, len);
      return ptr;
    }
    function stringsToPtr(strs) {
      const len = strs.length;
      const ptr = Module._malloc(len * SIZE_I32);
      for (let i = 0; i < len; i++) {
        Module.setValue(ptr + SIZE_I32 * i, stringToPtr(strs[i]), "i32");
      }
      return ptr;
    }
    function print(message) {
      Module.logger({
        type: "stdout",
        message: message
      });
    }
    function printErr(message) {
      if (!message.startsWith("Aborted(native code called abort())")) {
        Module.logger({
          type: "stderr",
          message: message
        });
      }
    }
    function exec(..._args) {
      const args = [...Module.DEFAULT_ARGS, ..._args];
      try {
        Module._ffmpeg(args.length, stringsToPtr(args));
      } catch (e) {
        if (!e.message.startsWith("Aborted")) {
          throw e;
        }
      }
      return Module.ret;
    }
    function setLogger(logger) {
      Module.logger = logger;
    }
    function setTimeout(timeout) {
      Module.timeout = timeout;
    }
    function setProgress(handler) {
      Module.progress = handler;
    }
    function receiveProgress(progress, time) {
      Module.progress({
        progress: progress,
        time: time
      });
    }
    function reset() {
      Module.ret = -1;
      Module.timeout = -1;
    }
    function _locateFile(path, prefix) {
      const mainScriptUrlOrBlob = Module.mainScriptUrlOrBlob;
      if (mainScriptUrlOrBlob) {
        const {
          wasmURL: wasmURL,
          workerURL: workerURL
        } = JSON.parse(atob(mainScriptUrlOrBlob.slice(mainScriptUrlOrBlob.lastIndexOf("#") + 1)));
        if (path.endsWith(".wasm")) {
          return wasmURL;
        }
        if (path.endsWith(".worker.js")) {
          return workerURL;
        }
      }
      return prefix + path;
    }
    Module.stringToPtr = stringToPtr;
    Module.stringsToPtr = stringsToPtr;
    Module.print = print;
    Module.printErr = printErr;
    Module.locateFile = _locateFile;
    Module.exec = exec;
    Module.setLogger = setLogger;
    Module.setTimeout = setTimeout;
    Module.setProgress = setProgress;
    Module.reset = reset;
    Module.receiveProgress = receiveProgress;
    var moduleOverrides = Object.assign({}, Module);
    var arguments_ = [];
    var thisProgram = "./this.program";
    var quit_ = (status, toThrow) => {
      throw toThrow;
    };
    var ENVIRONMENT_IS_WEB = typeof window == "object";
    var ENVIRONMENT_IS_WORKER = typeof importScripts == "function";
    var ENVIRONMENT_IS_NODE = typeof process == "object" && typeof process.versions == "object" && typeof process.versions.node == "string";
    var scriptDirectory = "";
    function locateFile(path) {
      if (Module.locateFile) {
        return Module.locateFile(path, scriptDirectory);
      }
      return scriptDirectory + path;
    }
    var read_;
    var readAsync;
    var readBinary;
    var setWindowTitle;
    if (ENVIRONMENT_IS_NODE) {
      const {
        createRequire: createRequire
      } = await import("module");
      var require = createRequire(import.meta.url);
      var fs = require("fs");
      var nodePath = require("path");
      if (ENVIRONMENT_IS_WORKER) {
        scriptDirectory = nodePath.dirname(scriptDirectory) + "/";
      } else {
        scriptDirectory = require("url").fileURLToPath(new URL("./", import.meta.url));
      }
      read_ = (filename, binary) => {
        filename = filename.startsWith("file://") ? new URL(filename) : nodePath.normalize(filename);
        return fs.readFileSync(filename, binary ? undefined : "utf8");
      };
      readBinary = filename => {
        var ret = read_(filename, true);
        if (!ret.buffer) {
          ret = new Uint8Array(ret);
        }
        return ret;
      };
      readAsync = (filename, onload, onerror, binary = true) => {
        filename = filename.startsWith("file://") ? new URL(filename) : nodePath.normalize(filename);
        fs.readFile(filename, binary ? undefined : "utf8", (err, data) => {
          if (err) {
            onerror(err);
          } else {
            onload(binary ? data.buffer : data);
          }
        });
      };
      if (!Module.thisProgram && process.argv.length > 1) {
        thisProgram = process.argv[1].replace(/\\/g, "/");
      }
      arguments_ = process.argv.slice(2);
      quit_ = (status, toThrow) => {
        process.exitCode = status;
        throw toThrow;
      };
      Module.inspect = () => "[Emscripten Module object]";
    } else if (ENVIRONMENT_IS_WEB || ENVIRONMENT_IS_WORKER) {
      if (ENVIRONMENT_IS_WORKER) {
        scriptDirectory = self.location.href;
      } else if (typeof document != "undefined" && document.currentScript) {
        scriptDirectory = document.currentScript.src;
      }
      if (_scriptDir) {
        scriptDirectory = _scriptDir;
      }
      if (scriptDirectory.indexOf("blob:") !== 0) {
        scriptDirectory = scriptDirectory.substr(0, scriptDirectory.replace(/[?#].*/, "").lastIndexOf("/") + 1);
      } else {
        scriptDirectory = "";
      }
      {
        read_ = url => {
          var xhr = new XMLHttpRequest();
          xhr.open("GET", url, false);
          xhr.send(null);
          return xhr.responseText;
        };
        if (ENVIRONMENT_IS_WORKER) {
          readBinary = url => {
            var xhr = new XMLHttpRequest();
            xhr.open("GET", url, false);
            xhr.responseType = "arraybuffer";
            xhr.send(null);
            return new Uint8Array(xhr.response);
          };
        }
        readAsync = (url, onload, onerror) => {
          var xhr = new XMLHttpRequest();
          xhr.open("GET", url, true);
          xhr.responseType = "arraybuffer";
          xhr.onload = () => {
            if (xhr.status == 200 || xhr.status == 0 && xhr.response) {
              onload(xhr.response);
              return;
            }
            onerror();
          };
          xhr.onerror = onerror;
          xhr.send(null);
        };
      }
      setWindowTitle = title => document.title = title;
    } else {}
    var out = Module.print || console.log.bind(console);
    var err = Module.printErr || console.error.bind(console);
    Object.assign(Module, moduleOverrides);
    moduleOverrides = null;
    if (Module.arguments) {
      arguments_ = Module.arguments;
    }
    if (Module.thisProgram) {
      thisProgram = Module.thisProgram;
    }
    if (Module.quit) {
      quit_ = Module.quit;
    }
    var wasmBinary;
    if (Module.wasmBinary) {
      wasmBinary = Module.wasmBinary;
    }
    if (typeof WebAssembly != "object") {
      abort("no native wasm support detected");
    }
    var ABORT = false;
    var EXITSTATUS;
    function assert(condition, text) {
      if (!condition) {
        abort(text);
      }
    }
    var HEAP8;
    var HEAPU8;
    var HEAP16;
    var HEAP32;
    var HEAPU32;
    var HEAPF32;
    var HEAP64;
    var HEAPF64;
    var __ATPRERUN__ = [];
    var __ATINIT__ = [];
    var __ATPOSTRUN__ = [];
    var runtimeInitialized = false;
    function preRun() {
      if (Module.preRun) {
        if (typeof Module.preRun == "function") {
          Module.preRun = [Module.preRun];
        }
        while (Module.preRun.length) {
          addOnPreRun(Module.preRun.shift());
        }
      }
      callRuntimeCallbacks(__ATPRERUN__);
    }
    function initRuntime() {
      runtimeInitialized = true;
      if (!Module.noFSInit && !FS.init.initialized) {
        FS.init();
      }
      FS.ignorePermissions = false;
      TTY.init();
      SOCKFS.root = FS.mount(SOCKFS, {}, null);
      callRuntimeCallbacks(__ATINIT__);
    }
    function postRun() {
      if (Module.postRun) {
        if (typeof Module.postRun == "function") {
          Module.postRun = [Module.postRun];
        }
        while (Module.postRun.length) {
          addOnPostRun(Module.postRun.shift());
        }
      }
      callRuntimeCallbacks(__ATPOSTRUN__);
    }
    function addOnPreRun(cb) {
      __ATPRERUN__.unshift(cb);
    }
    function addOnPostRun(cb) {
      __ATPOSTRUN__.unshift(cb);
    }
    var runDependencies = 0;
    var runDependencyWatcher = null;
    var dependenciesFulfilled = null;
    function addRunDependency(id) {
      runDependencies++;
      if (Module.monitorRunDependencies) {
        Module.monitorRunDependencies(runDependencies);
      }
    }
    function removeRunDependency(id) {
      runDependencies--;
      if (Module.monitorRunDependencies) {
        Module.monitorRunDependencies(runDependencies);
      }
      if (runDependencies == 0) {
        if (runDependencyWatcher !== null) {
          clearInterval(runDependencyWatcher);
          runDependencyWatcher = null;
        }
        if (dependenciesFulfilled) {
          var callback = dependenciesFulfilled;
          dependenciesFulfilled = null;
          callback();
        }
      }
    }
    function abort(what) {
      if (Module.onAbort) {
        Module.onAbort(what);
      }
      what = "Aborted(" + what + ")";
      err(what);
      ABORT = true;
      EXITSTATUS = 1;
      what += ". Build with -sASSERTIONS for more info.";
      var e = new WebAssembly.RuntimeError(what);
      readyPromiseReject(e);
      throw e;
    }
    var wasmBinaryFile;
    if (Module.locateFile) {
      wasmBinaryFile = "ffmpeg-core.wasm";
      if (!wasmBinaryFile.startsWith("data:application/octet-stream;base64,")) {
        wasmBinaryFile = locateFile(wasmBinaryFile);
      }
    } else {
      wasmBinaryFile = new URL("ffmpeg-core.wasm", import.meta.url).href;
    }
    function callRuntimeCallbacks(callbacks) {
      while (callbacks.length > 0) {
        callbacks.shift()(Module);
      }
    }
    function getValue(ptr, type = "i8") {
      if (type.endsWith("*")) {
        type = "*";
      }
      switch (type) {
        case "i1":
          return HEAP8[ptr >> 0];
        case "i8":
          return HEAP8[ptr >> 0];
        case "i16":
          return HEAP16[ptr >> 1];
        case "i32":
          return HEAP32[ptr >> 2];
        case "i64":
          return HEAP64[ptr >> 3];
        case "float":
          return HEAPF32[ptr >> 2];
        case "double":
          return HEAPF64[ptr >> 3];
        case "*":
          return HEAPU32[ptr >> 2];
        default:
          abort(`invalid type for getValue: ${type}`);
      }
    }
    function setValue(ptr, value, type = "i8") {
      if (type.endsWith("*")) {
        type = "*";
      }
      switch (type) {
        case "i1":
          HEAP8[ptr >> 0] = value;
          break;
        case "i8":
          HEAP8[ptr >> 0] = value;
          break;
        case "i16":
          HEAP16[ptr >> 1] = value;
          break;
        case "i32":
          HEAP32[ptr >> 2] = value;
          break;
        case "i64":
          HEAP64[ptr >> 3] = BigInt(value);
          break;
        case "float":
          HEAPF32[ptr >> 2] = value;
          break;
        case "double":
          HEAPF64[ptr >> 3] = value;
          break;
        case "*":
          HEAPU32[ptr >> 2] = value;
          break;
        default:
          abort(`invalid type for setValue: ${type}`);
      }
    }
    var UTF8Decoder = typeof TextDecoder != "undefined" ? new TextDecoder("utf8") : undefined;
    function UTF8ArrayToString(heapOrArray, idx, maxBytesToRead) {
      var endIdx = idx + maxBytesToRead;
      var endPtr = idx;
      while (heapOrArray[endPtr] && !(endPtr >= endIdx)) {
        ++endPtr;
      }
      if (endPtr - idx > 16 && heapOrArray.buffer && UTF8Decoder) {
        return UTF8Decoder.decode(heapOrArray.subarray(idx, endPtr));
      }
      var str = "";
      while (idx < endPtr) {
        var u0 = heapOrArray[idx++];
        if (!(u0 & 128)) {
          str += String.fromCharCode(u0);
          continue;
        }
        var u1 = heapOrArray[idx++] & 63;
        if ((u0 & 224) == 192) {
          str += String.fromCharCode((u0 & 31) << 6 | u1);
          continue;
        }
        var u2 = heapOrArray[idx++] & 63;
        if ((u0 & 240) == 224) {
          u0 = (u0 & 15) << 12 | u1 << 6 | u2;
        } else {
          u0 = (u0 & 7) << 18 | u1 << 12 | u2 << 6 | heapOrArray[idx++] & 63;
        }
        if (u0 < 65536) {
          str += String.fromCharCode(u0);
        } else {
          var ch = u0 - 65536;
          str += String.fromCharCode(55296 | ch >> 10, 56320 | ch & 1023);
        }
      }
      return str;
    }
    function UTF8ToString(ptr, maxBytesToRead) {
      return ptr ? UTF8ArrayToString(HEAPU8, ptr, maxBytesToRead) : "";
    }
    var PATH = {
      isAbs: path => path.charAt(0) === "/",
      splitPath: filename => {
        var splitPathRe = /^(\/?|)([\s\S]*?)((?:\.{1,2}|[^\/]+?|)(\.[^.\/]*|))(?:[\/]*)$/;
        return splitPathRe.exec(filename).slice(1);
      },
      normalizeArray: (parts, allowAboveRoot) => {
        var up = 0;
        for (var i = parts.length - 1; i >= 0; i--) {
          var last = parts[i];
          if (last === ".") {
            parts.splice(i, 1);
          } else if (last === "..") {
            parts.splice(i, 1);
            up++;
          } else if (up) {
            parts.splice(i, 1);
            up--;
          }
        }
        if (allowAboveRoot) {
          for (; up; up--) {
            parts.unshift("..");
          }
        }
        return parts;
      },
      normalize: path => {
        var isAbsolute = path.charAt(0) === "/";
        var trailingSlash = path.substr(-1) === "/";
        path = PATH.normalizeArray(path.split("/").filter(p => !!p), !isAbsolute).join("/");
        if (!path && !isAbsolute) {
          path = ".";
        }
        if (path && trailingSlash) {
          path += "/";
        }
        return (isAbsolute ? "/" : "") + path;
      },
      dirname: path => {
        var result = PATH.splitPath(path);
        var root = result[0];
        var dir = result[1];
        if (!root && !dir) {
          return ".";
        }
        if (dir) {
          dir = dir.substr(0, dir.length - 1);
        }
        return root + dir;
      },
      basename: path => {
        if (path === "/") {
          return "/";
        }
        path = PATH.normalize(path);
        path = path.replace(/\/$/, "");
        var lastSlash = path.lastIndexOf("/");
        if (lastSlash === -1) {
          return path;
        }
        return path.substr(lastSlash + 1);
      },
      join: function () {
        var paths = Array.prototype.slice.call(arguments);
        return PATH.normalize(paths.join("/"));
      },
      join2: (l, r) => {
        return PATH.normalize(l + "/" + r);
      }
    };
    function initRandomFill() {
      if (typeof crypto == "object" && typeof crypto.getRandomValues == "function") {
        return view => crypto.getRandomValues(view);
      } else if (ENVIRONMENT_IS_NODE) {
        try {
          var crypto_module = require("crypto");
          var randomFillSync = crypto_module.randomFillSync;
          if (randomFillSync) {
            return view => crypto_module.randomFillSync(view);
          }
          var randomBytes = crypto_module.randomBytes;
          return view => (view.set(randomBytes(view.byteLength)), view);
        } catch (e) {}
      }
      abort("initRandomDevice");
    }
    function randomFill(view) {
      return (randomFill = initRandomFill())(view);
    }
    var PATH_FS = {
      resolve: function () {
        var resolvedPath = "";
        var resolvedAbsolute = false;
        for (var i = arguments.length - 1; i >= -1 && !resolvedAbsolute; i--) {
          var path = i >= 0 ? arguments[i] : "/";
          if (typeof path != "string") {
            throw new TypeError("Arguments to path.resolve must be strings");
          } else if (!path) {
            return "";
          }
          resolvedPath = path + "/" + resolvedPath;
          resolvedAbsolute = path.charAt(0) === "/";
        }
        resolvedPath = PATH.normalizeArray(resolvedPath.split("/").filter(p => !!p), !resolvedAbsolute).join("/");
        return (resolvedAbsolute ? "/" : "") + resolvedPath || ".";
      },
      relative: (from, to) => {
        from = PATH_FS.resolve(from).substr(1);
        to = PATH_FS.resolve(to).substr(1);
        function trim(arr) {
          var start = 0;
          for (; start < arr.length; start++) {
            if (arr[start] !== "") {
              break;
            }
          }
          var end = arr.length - 1;
          for (; end >= 0; end--) {
            if (arr[end] !== "") {
              break;
            }
          }
          if (start > end) {
            return [];
          }
          return arr.slice(start, end - start + 1);
        }
        var fromParts = trim(from.split("/"));
        var toParts = trim(to.split("/"));
        var length = Math.min(fromParts.length, toParts.length);
        var samePartsLength = length;
        for (var i = 0; i < length; i++) {
          if (fromParts[i] !== toParts[i]) {
            samePartsLength = i;
            break;
          }
        }
        var outputParts = [];
        for (var i = samePartsLength; i < fromParts.length; i++) {
          outputParts.push("..");
        }
        outputParts = outputParts.concat(toParts.slice(samePartsLength));
        return outputParts.join("/");
      }
    };
    function lengthBytesUTF8(str) {
      var len = 0;
      for (var i = 0; i < str.length; ++i) {
        var c = str.charCodeAt(i);
        if (c <= 127) {
          len++;
        } else if (c <= 2047) {
          len += 2;
        } else if (c >= 55296 && c <= 57343) {
          len += 4;
          ++i;
        } else {
          len += 3;
        }
      }
      return len;
    }
    function stringToUTF8Array(str, heap, outIdx, maxBytesToWrite) {
      if (!(maxBytesToWrite > 0)) {
        return 0;
      }
      var startIdx = outIdx;
      var endIdx = outIdx + maxBytesToWrite - 1;
      for (var i = 0; i < str.length; ++i) {
        var u = str.charCodeAt(i);
        if (u >= 55296 && u <= 57343) {
          var u1 = str.charCodeAt(++i);
          u = 65536 + ((u & 1023) << 10) | u1 & 1023;
        }
        if (u <= 127) {
          if (outIdx >= endIdx) {
            break;
          }
          heap[outIdx++] = u;
        } else if (u <= 2047) {
          if (outIdx + 1 >= endIdx) {
            break;
          }
          heap[outIdx++] = 192 | u >> 6;
          heap[outIdx++] = 128 | u & 63;
        } else if (u <= 65535) {
          if (outIdx + 2 >= endIdx) {
            break;
          }
          heap[outIdx++] = 224 | u >> 12;
          heap[outIdx++] = 128 | u >> 6 & 63;
          heap[outIdx++] = 128 | u & 63;
        } else {
          if (outIdx + 3 >= endIdx) {
            break;
          }
          heap[outIdx++] = 240 | u >> 18;
          heap[outIdx++] = 128 | u >> 12 & 63;
          heap[outIdx++] = 128 | u >> 6 & 63;
          heap[outIdx++] = 128 | u & 63;
        }
      }
      heap[outIdx] = 0;
      return outIdx - startIdx;
    }
    function intArrayFromString(stringy, dontAddNull, length) {
      var len = length > 0 ? length : lengthBytesUTF8(stringy) + 1;
      var u8array = new Array(len);
      var numBytesWritten = stringToUTF8Array(stringy, u8array, 0, u8array.length);
      if (dontAddNull) {
        u8array.length = numBytesWritten;
      }
      return u8array;
    }
    var TTY = {
      ttys: [],
      init: function () {},
      shutdown: function () {},
      register: function (dev, ops) {
        TTY.ttys[dev] = {
          input: [],
          output: [],
          ops: ops
        };
        FS.registerDevice(dev, TTY.stream_ops);
      },
      stream_ops: {
        open: function (stream) {
          var tty = TTY.ttys[stream.node.rdev];
          if (!tty) {
            throw new null(43);
          }
          stream.tty = tty;
          stream.seekable = false;
        },
        close: function (stream) {
          stream.tty.ops.fsync(stream.tty);
        },
        fsync: function (stream) {
          stream.tty.ops.fsync(stream.tty);
        },
        read: function (stream, buffer, offset, length, pos) {
          if (!stream.tty || !stream.tty.ops.get_char) {
            throw new null(60);
          }
          var bytesRead = 0;
          for (var i = 0; i < length; i++) {
            var result;
            try {
              result = stream.tty.ops.get_char(stream.tty);
            } catch (e) {
              throw new null(29);
            }
            if (result === undefined && bytesRead === 0) {
              throw new null(6);
            }
            if (result === null || result === undefined) {
              break;
            }
            bytesRead++;
            buffer[offset + i] = result;
          }
          if (bytesRead) {
            stream.node.timestamp = Date.now();
          }
          return bytesRead;
        },
        write: function (stream, buffer, offset, length, pos) {
          if (!stream.tty || !stream.tty.ops.put_char) {
            throw new null(60);
          }
          try {
            for (var i = 0; i < length; i++) {
              stream.tty.ops.put_char(stream.tty, buffer[offset + i]);
            }
          } catch (e) {
            throw new null(29);
          }
          if (length) {
            stream.node.timestamp = Date.now();
          }
          return i;
        }
      },
      default_tty_ops: {
        get_char: function (tty) {
          if (!tty.input.length) {
            var result = null;
            if (ENVIRONMENT_IS_NODE) {
              var buf = Buffer.alloc(256);
              var bytesRead = 0;
              try {
                bytesRead = fs.readSync(process.stdin.fd, buf, 0, 256, -1);
              } catch (e) {
                if (e.toString().includes("EOF")) {
                  bytesRead = 0;
                } else {
                  throw e;
                }
              }
              if (bytesRead > 0) {
                result = buf.slice(0, bytesRead).toString("utf-8");
              } else {
                result = null;
              }
            } else if (typeof window != "undefined" && typeof window.prompt == "function") {
              result = window.prompt("Input: ");
              if (result !== null) {
                result += "\n";
              }
            } else if (typeof readline == "function") {
              result = readline();
              if (result !== null) {
                result += "\n";
              }
            }
            if (!result) {
              return null;
            }
            tty.input = intArrayFromString(result, true);
          }
          return tty.input.shift();
        },
        put_char: function (tty, val) {
          if (val === null || val === 10) {
            out(UTF8ArrayToString(tty.output, 0));
            tty.output = [];
          } else {
            if (val != 0) {
              tty.output.push(val);
            }
          }
        },
        fsync: function (tty) {
          if (tty.output && tty.output.length > 0) {
            out(UTF8ArrayToString(tty.output, 0));
            tty.output = [];
          }
        }
      },
      default_tty1_ops: {
        put_char: function (tty, val) {
          if (val === null || val === 10) {
            err(UTF8ArrayToString(tty.output, 0));
            tty.output = [];
          } else {
            if (val != 0) {
              tty.output.push(val);
            }
          }
        },
        fsync: function (tty) {
          if (tty.output && tty.output.length > 0) {
            err(UTF8ArrayToString(tty.output, 0));
            tty.output = [];
          }
        }
      }
    };
    function zeroMemory(address, size) {
      HEAPU8.fill(0, address, address + size);
      return address;
    }
    function mmapAlloc(size) {
      size = Math.ceil(size / 65536) * 65536;
      var ptr = _emscripten_builtin_memalign(65536, size);
      if (!ptr) {
        return 0;
      }
      return zeroMemory(ptr, size);
    }
    var MEMFS = {
      ops_table: null,
      mount: function (mount) {
        return MEMFS.createNode(null, "/", 16895, 0);
      },
      createNode: function (parent, name, mode, dev) {
        if ((mode & 61440) === 24576 || (mode & 61440) === 4096) {
          throw new null(63);
        }
        MEMFS.ops_table = {
          dir: {
            node: {
              getattr: MEMFS.node_ops.getattr,
              setattr: MEMFS.node_ops.setattr,
              lookup: MEMFS.node_ops.lookup,
              mknod: MEMFS.node_ops.mknod,
              rename: MEMFS.node_ops.rename,
              unlink: MEMFS.node_ops.unlink,
              rmdir: MEMFS.node_ops.rmdir,
              readdir: MEMFS.node_ops.readdir,
              symlink: MEMFS.node_ops.symlink
            },
            stream: {
              llseek: MEMFS.stream_ops.llseek
            }
          },
          file: {
            node: {
              getattr: MEMFS.node_ops.getattr,
              setattr: MEMFS.node_ops.setattr
            },
            stream: {
              llseek: MEMFS.stream_ops.llseek,
              read: MEMFS.stream_ops.read,
              write: MEMFS.stream_ops.write,
              allocate: MEMFS.stream_ops.allocate,
              mmap: MEMFS.stream_ops.mmap,
              msync: MEMFS.stream_ops.msync
            }
          },
          link: {
            node: {
              getattr: MEMFS.node_ops.getattr,
              setattr: MEMFS.node_ops.setattr,
              readlink: MEMFS.node_ops.readlink
            },
            stream: {}
          },
          chrdev: {
            node: {
              getattr: MEMFS.node_ops.getattr,
              setattr: MEMFS.node_ops.setattr
            },
            stream: FS.chrdev_stream_ops
          }
        };
        var node = FS.createNode(parent, name, mode, dev);
        if ((node.mode & 61440) === 16384) {
          node.node_ops = null.dir.node;
          node.stream_ops = null.dir.stream;
          node.contents = {};
        } else if ((node.mode & 61440) === 32768) {
          node.node_ops = null.file.node;
          node.stream_ops = null.file.stream;
          node.usedBytes = 0;
          node.contents = null;
        } else if ((node.mode & 61440) === 40960) {
          node.node_ops = null.link.node;
          node.stream_ops = null.link.stream;
        } else if ((node.mode & 61440) === 8192) {
          node.node_ops = null.chrdev.node;
          node.stream_ops = null.chrdev.stream;
        }
        node.timestamp = Date.now();
        if (parent) {
          parent.contents[name] = node;
          parent.timestamp = node.timestamp;
        }
        return node;
      },
      getFileDataAsTypedArray: function (node) {
        if (!node.contents) {
          return new Uint8Array(0);
        }
        if (node.contents.subarray) {
          return node.contents.subarray(0, node.usedBytes);
        }
        return new Uint8Array(node.contents);
      },
      expandFileStorage: function (node, newCapacity) {
        var prevCapacity = node.contents ? node.contents.length : 0;
        if (prevCapacity >= newCapacity) {
          return;
        }
        newCapacity = Math.max(newCapacity, prevCapacity * (prevCapacity < 1048576 ? 2 : 1.125) >>> 0);
        if (prevCapacity != 0) {
          newCapacity = Math.max(newCapacity, 256);
        }
        var oldContents = node.contents;
        node.contents = new Uint8Array(newCapacity);
        if (node.usedBytes > 0) {
          node.contents.set(oldContents.subarray(0, node.usedBytes), 0);
        }
      },
      resizeFileStorage: function (node, newSize) {
        if (node.usedBytes == newSize) {
          return;
        }
        if (newSize == 0) {
          node.contents = null;
          node.usedBytes = 0;
        } else {
          var oldContents = node.contents;
          node.contents = new Uint8Array(newSize);
          if (oldContents) {
            node.contents.set(oldContents.subarray(0, Math.min(newSize, node.usedBytes)));
          }
          node.usedBytes = newSize;
        }
      },
      node_ops: {
        getattr: function (node) {
          var attr = {
            dev: (node.mode & 61440) === 8192 ? node.id : 1,
            ino: node.id,
            mode: node.mode,
            nlink: 1,
            uid: 0,
            gid: 0,
            rdev: node.rdev
          };
          if ((node.mode & 61440) === 16384) {
            attr.size = 4096;
          } else if ((node.mode & 61440) === 32768) {
            attr.size = node.usedBytes;
          } else if ((node.mode & 61440) === 40960) {
            attr.size = node.link.length;
          } else {
            attr.size = 0;
          }
          attr.atime = new Date(node.timestamp);
          attr.mtime = new Date(node.timestamp);
          attr.ctime = new Date(node.timestamp);
          attr.blksize = 4096;
          attr.blocks = Math.ceil(attr.size / attr.blksize);
          return attr;
        },
        setattr: function (node, attr) {
          if (attr.mode !== undefined) {
            node.mode = attr.mode;
          }
          if (attr.timestamp !== undefined) {
            node.timestamp = attr.timestamp;
          }
          if (attr.size !== undefined) {
            MEMFS.resizeFileStorage(node, attr.size);
          }
        },
        lookup: function (parent, name) {
          throw FS.genericErrors[44];
        },
        mknod: function (parent, name, mode, dev) {
          return MEMFS.createNode(parent, name, mode, dev);
        },
        rename: function (old_node, new_dir, new_name) {
          if ((old_node.mode & 61440) === 16384) {
            var new_node;
            try {
              new_node = FS.lookupNode(new_dir, new_name);
            } catch (e) {}
            if (new_node) {
              for (var i in new_node.contents) {
                throw new null(55);
              }
            }
          }
          delete old_node.parent.contents[old_node.name];
          old_node.parent.timestamp = Date.now();
          old_node.name = new_name;
          new_dir.contents[new_name] = old_node;
          new_dir.timestamp = old_node.parent.timestamp;
          old_node.parent = new_dir;
        },
        unlink: function (parent, name) {
          delete parent.contents[name];
          parent.timestamp = Date.now();
        },
        rmdir: function (parent, name) {
          var node = FS.lookupNode(parent, name);
          for (var i in node.contents) {
            throw new null(55);
          }
          delete parent.contents[name];
          parent.timestamp = Date.now();
        },
        readdir: function (node) {
          var entries = [".", ".."];
          for (var key in node.contents) {
            if (!node.contents.hasOwnProperty(key)) {
              continue;
            }
            entries.push(key);
          }
          return entries;
        },
        symlink: function (parent, newname, oldpath) {
          var node = MEMFS.createNode(parent, newname, 41471, 0);
          node.link = oldpath;
          return node;
        },
        readlink: function (node) {
          if (!((node.mode & 61440) === 40960)) {
            throw new null(28);
          }
          return node.link;
        }
      },
      stream_ops: {
        read: function (stream, buffer, offset, length, position) {
          var contents = stream.node.contents;
          if (position >= stream.node.usedBytes) {
            return 0;
          }
          var size = Math.min(stream.node.usedBytes - position, length);
          if (size > 8 && contents.subarray) {
            buffer.set(contents.subarray(position, position + size), offset);
          } else {
            for (var i = 0; i < size; i++) {
              buffer[offset + i] = contents[position + i];
            }
          }
          return size;
        },
        write: function (stream, buffer, offset, length, position, canOwn) {
          if (buffer.buffer === HEAP8.buffer) {
            canOwn = false;
          }
          if (!length) {
            return 0;
          }
          var node = stream.node;
          node.timestamp = Date.now();
          if (buffer.subarray && (!node.contents || node.contents.subarray)) {
            if (canOwn) {
              node.contents = buffer.subarray(offset, offset + length);
              node.usedBytes = length;
              return length;
            } else if (node.usedBytes === 0 && position === 0) {
              node.contents = buffer.slice(offset, offset + length);
              node.usedBytes = length;
              return length;
            } else if (position + length <= node.usedBytes) {
              node.contents.set(buffer.subarray(offset, offset + length), position);
              return length;
            }
          }
          MEMFS.expandFileStorage(node, position + length);
          if (node.contents.subarray && buffer.subarray) {
            node.contents.set(buffer.subarray(offset, offset + length), position);
          } else {
            for (var i = 0; i < length; i++) {
              node.contents[position + i] = buffer[offset + i];
            }
          }
          node.usedBytes = Math.max(node.usedBytes, position + length);
          return length;
        },
        llseek: function (stream, offset, whence) {
          var position = offset;
          if (whence === 1) {
            position += stream.position;
          } else if (whence === 2) {
            if ((stream.node.mode & 61440) === 32768) {
              position += stream.node.usedBytes;
            }
          }
          if (position < 0) {
            throw new null(28);
          }
          return position;
        },
        allocate: function (stream, offset, length) {
          MEMFS.expandFileStorage(stream.node, offset + length);
          stream.node.usedBytes = Math.max(stream.node.usedBytes, offset + length);
        },
        mmap: function (stream, length, position, prot, flags) {
          if (!((stream.node.mode & 61440) === 32768)) {
            throw new null(43);
          }
          var ptr;
          var allocated;
          var contents = stream.node.contents;
          if (!(flags & 2) && contents.buffer === HEAP8.buffer) {
            allocated = false;
            ptr = contents.byteOffset;
          } else {
            if (position > 0 || position + length < contents.length) {
              if (contents.subarray) {
                contents = contents.subarray(position, position + length);
              } else {
                contents = Array.prototype.slice.call(contents, position, position + length);
              }
            }
            allocated = true;
            ptr = mmapAlloc(length);
            if (!ptr) {
              throw new null(48);
            }
            HEAP8.set(contents, ptr);
          }
          return {
            ptr: ptr,
            allocated: allocated
          };
        },
        msync: function (stream, buffer, offset, length, mmapFlags) {
          MEMFS.stream_ops.write(stream, buffer, 0, length, offset, false);
          return 0;
        }
      }
    };
    function asyncLoad(url, onload, onerror, noRunDep) {
      var dep = !noRunDep ? id : "";
      readAsync(url, arrayBuffer => {
        assert(arrayBuffer, `Loading data file "${url}" failed (no arrayBuffer).`);
        onload(new Uint8Array(arrayBuffer));
        if (dep) {
          removeRunDependency(dep);
        }
      }, event => {
        if (onerror) {
          onerror();
        } else {
          throw `Loading data file "${url}" failed.`;
        }
      });
      if (dep) {
        addRunDependency(dep);
      }
    }
    var preloadPlugins = Module.preloadPlugins || [];
    function FS_handledByPreloadPlugin(byteArray, fullname, finish, onerror) {
      if (typeof Browser != "undefined") {
        Browser.init();
      }
      var handled = false;
      preloadPlugins.forEach(function (plugin) {
        if (handled) {
          return;
        }
        if (plugin.canHandle(fullname)) {
          plugin.handle(byteArray, fullname, finish, onerror);
          handled = true;
        }
      });
      return handled;
    }
    function FS_createPreloadedFile(parent, name, url, canRead, canWrite, onload, onerror, dontCreateFile, canOwn, preFinish) {
      var fullname = name ? PATH_FS.resolve(PATH.normalize(parent + "/" + name)) : parent;
      function processData(byteArray) {
        function finish(byteArray) {
          if (preFinish) {
            preFinish();
          }
          if (!dontCreateFile) {
            FS.createDataFile(parent, name, byteArray, canRead, canWrite, canOwn);
          }
          if (onload) {
            onload();
          }
          removeRunDependency(id);
        }
        if (FS_handledByPreloadPlugin(byteArray, fullname, finish, () => {
          if (onerror) {
            onerror();
          }
          removeRunDependency(id);
        })) {
          return;
        }
        finish(byteArray);
      }
      addRunDependency(id);
      if (typeof url == "string") {
        asyncLoad(url, byteArray => processData(byteArray), onerror);
      } else {
        processData(url);
      }
    }
    function FS_modeStringToFlags(str) {
      var flagModes = {
        "r": 0,
        "r+": 2,
        "w": 577,
        "w+": 578,
        "a": 1089,
        "a+": 1090
      };
      var flags = flagModes[str];
      if (typeof flags == "undefined") {
        throw new Error(`Unknown file open mode: ${str}`);
      }
      return flags;
    }
    function FS_getMode(canRead, canWrite) {
      var mode = 0;
      if (canRead) {
        mode |= 365;
      }
      if (canWrite) {
        mode |= 146;
      }
      return mode;
    }
    var WORKERFS = {
      DIR_MODE: 16895,
      FILE_MODE: 33279,
      reader: null,
      mount: function (mount) {
        assert(ENVIRONMENT_IS_WORKER);
        WORKERFS.reader = new FileReaderSync();
        var root = WORKERFS.createNode(null, "/", 16895, 0);
        var createdParents = {};
        function ensureParent(path) {
          var parts = path.split("/");
          var parent = root;
          for (var i = 0; i < parts.length - 1; i++) {
            var curr = parts.slice(0, i + 1).join("/");
            if (!createdParents[curr]) {
              createdParents[curr] = WORKERFS.createNode(parent, parts[i], 16895, 0);
            }
            parent = createdParents[curr];
          }
          return parent;
        }
        function base(path) {
          var parts = path.split("/");
          return parts[parts.length - 1];
        }
        Array.prototype.forEach.call(mount.opts.files || [], function (file) {
          WORKERFS.createNode(ensureParent(file.name), base(file.name), 33279, 0, file, file.lastModifiedDate);
        });
        (mount.opts.blobs || []).forEach(function (obj) {
          WORKERFS.createNode(ensureParent(obj.name), base(obj.name), 33279, 0, obj.data);
        });
        (mount.opts.packages || []).forEach(function (pack) {
          pack.metadata.files.forEach(function (file) {
            var name = file.filename.substr(1);
            WORKERFS.createNode(ensureParent(name), base(name), 33279, 0, pack.blob.slice(file.start, file.end));
          });
        });
        return root;
      },
      createNode: function (parent, name, mode, dev, contents, mtime) {
        var node = FS.createNode(parent, name, mode);
        node.mode = mode;
        node.node_ops = WORKERFS.node_ops;
        node.stream_ops = WORKERFS.stream_ops;
        node.timestamp = (mtime || new Date()).getTime();
        assert(true);
        if (mode === 33279) {
          node.size = contents.size;
          node.contents = contents;
        } else {
          node.size = 4096;
          node.contents = {};
        }
        if (parent) {
          parent.contents[name] = node;
        }
        return node;
      },
      node_ops: {
        getattr: function (node) {
          return {
            dev: 1,
            ino: node.id,
            mode: node.mode,
            nlink: 1,
            uid: 0,
            gid: 0,
            rdev: undefined,
            size: node.size,
            atime: new Date(node.timestamp),
            mtime: new Date(node.timestamp),
            ctime: new Date(node.timestamp),
            blksize: 4096,
            blocks: Math.ceil(node.size / 4096)
          };
        },
        setattr: function (node, attr) {
          if (attr.mode !== undefined) {
            node.mode = attr.mode;
          }
          if (attr.timestamp !== undefined) {
            node.timestamp = attr.timestamp;
          }
        },
        lookup: function (parent, name) {
          throw new null(44);
        },
        mknod: function (parent, name, mode, dev) {
          throw new null(63);
        },
        rename: function (oldNode, newDir, newName) {
          throw new null(63);
        },
        unlink: function (parent, name) {
          throw new null(63);
        },
        rmdir: function (parent, name) {
          throw new null(63);
        },
        readdir: function (node) {
          var entries = [".", ".."];
          for (var key in node.contents) {
            if (!node.contents.hasOwnProperty(key)) {
              continue;
            }
            entries.push(key);
          }
          return entries;
        },
        symlink: function (parent, newName, oldPath) {
          throw new null(63);
        }
      },
      stream_ops: {
        read: function (stream, buffer, offset, length, position) {
          if (position >= stream.node.size) {
            return 0;
          }
          var chunk = stream.node.contents.slice(position, position + length);
          var ab = null.readAsArrayBuffer(chunk);
          buffer.set(new Uint8Array(ab), offset);
          return chunk.size;
        },
        write: function (stream, buffer, offset, length, position) {
          throw new null(29);
        },
        llseek: function (stream, offset, whence) {
          var position = offset;
          if (whence === 1) {
            position += stream.position;
          } else if (whence === 2) {
            if ((stream.node.mode & 61440) === 32768) {
              position += stream.node.size;
            }
          }
          if (position < 0) {
            throw new null(28);
          }
          return position;
        }
      }
    };
    var FS = {
      root: null,
      mounts: [],
      devices: {},
      streams: [],
      nextInode: 1,
      nameTable: null,
      currentPath: "/",
      initialized: false,
      ignorePermissions: true,
      ErrnoError: null,
      genericErrors: {},
      filesystems: null,
      syncFSRequests: 0,
      lookupPath: (path, opts = {}) => {
        path = PATH_FS.resolve(path);
        if (!path) {
          return {
            path: "",
            node: null
          };
        }
        var defaults = {
          follow_mount: true,
          recurse_count: 0
        };
        opts = Object.assign(defaults, opts);
        if (opts.recurse_count > 8) {
          throw new null(32);
        }
        var parts = path.split("/").filter(p => !!p);
        var current = null;
        var current_path = "/";
        for (var i = 0; i < parts.length; i++) {
          var islast = i === parts.length - 1;
          if (islast && opts.parent) {
            break;
          }
          current = FS.lookupNode(current, parts[i]);
          current_path = PATH.normalize(current_path + "/" + parts[i]);
          if (!!current.mounted) {
            if (!islast || islast && opts.follow_mount) {
              current = current.mounted.root;
            }
          }
          if (!islast || opts.follow) {
            var count = 0;
            while ((current.mode & 61440) === 40960) {
              var link = FS.readlink(current_path);
              current_path = PATH_FS.resolve(PATH.dirname(current_path), link);
              var lookup = FS.lookupPath(current_path, {
                recurse_count: opts.recurse_count + 1
              });
              current = lookup.node;
              if (count++ > 40) {
                throw new null(32);
              }
            }
          }
        }
        return {
          path: current_path,
          node: current
        };
      },
      getPath: node => {
        var path;
        while (true) {
          if (node === node.parent) {
            var mount = node.mount.mountpoint;
            if (!path) {
              return mount;
            }
            return mount[mount.length - 1] !== "/" ? `${mount}/${path}` : mount + path;
          }
          path = path ? `${node.name}/${path}` : node.name;
          node = node.parent;
        }
      },
      hashName: (parentid, name) => {
        var hash = 0;
        for (var i = 0; i < name.length; i++) {
          hash = (hash << 5) - hash + name.charCodeAt(i) | 0;
        }
        return (parentid + hash >>> 0) % null.length;
      },
      hashAddNode: node => {
        var hash = FS.hashName(node.parent.id, node.name);
        node.name_next = null[hash];
        null[hash] = node;
      },
      hashRemoveNode: node => {
        var hash = FS.hashName(node.parent.id, node.name);
        if (null[hash] === node) {
          null[hash] = node.name_next;
        } else {
          var current = null[hash];
          while (current) {
            if (current.name_next === node) {
              current.name_next = node.name_next;
              break;
            }
            current = current.name_next;
          }
        }
      },
      lookupNode: (parent, name) => {
        var errCode = FS.mayLookup(parent);
        if (errCode) {
          throw new null(errCode, parent);
        }
        var hash = FS.hashName(parent.id, name);
        for (var node = null[hash]; node; node = node.name_next) {
          var nodeName = node.name;
          if (node.parent.id === parent.id && nodeName === name) {
            return node;
          }
        }
        return parent.node_ops.lookup(parent, name);
      },
      createNode: (parent, name, mode, rdev) => {
        var node = new FS.FSNode(parent, name, mode, rdev);
        FS.hashAddNode(node);
        return node;
      },
      destroyNode: node => {
        FS.hashRemoveNode(node);
      },
      isRoot: node => {
        return node === node.parent;
      },
      isMountpoint: node => {
        return !!node.mounted;
      },
      isFile: mode => {
        return (mode & 61440) === 32768;
      },
      isDir: mode => {
        return (mode & 61440) === 16384;
      },
      isLink: mode => {
        return (mode & 61440) === 40960;
      },
      isChrdev: mode => {
        return (mode & 61440) === 8192;
      },
      isBlkdev: mode => {
        return (mode & 61440) === 24576;
      },
      isFIFO: mode => {
        return (mode & 61440) === 4096;
      },
      isSocket: mode => {
        return (mode & 49152) === 49152;
      },
      flagsToPermissionString: flag => {
        var perms = ["r", "w", "rw"][flag & 3];
        if (flag & 512) {
          perms += "w";
        }
        return perms;
      },
      nodePermissions: (node, perms) => {
        return 0;
        if (perms.includes("r") && !(node.mode & 292)) {
          return 2;
        } else if (perms.includes("w") && !(node.mode & 146)) {
          return 2;
        } else if (perms.includes("x") && !(node.mode & 73)) {
          return 2;
        }
        return 0;
      },
      mayLookup: dir => {
        var errCode = FS.nodePermissions(dir, "x");
        if (errCode) {
          return errCode;
        }
        if (!dir.node_ops.lookup) {
          return 2;
        }
        return 0;
      },
      mayCreate: (dir, name) => {
        try {
          return 20;
        } catch (e) {}
        return FS.nodePermissions(dir, "wx");
      },
      mayDelete: (dir, name, isdir) => {
        var node;
        try {
          node = FS.lookupNode(dir, name);
        } catch (e) {
          return e.errno;
        }
        var errCode = FS.nodePermissions(dir, "wx");
        if (errCode) {
          return errCode;
        }
        if (isdir) {
          if (!((node.mode & 61440) === 16384)) {
            return 54;
          }
          if (node === node.parent || FS.getPath(node) === "/") {
            return 10;
          }
        } else {
          if ((node.mode & 61440) === 16384) {
            return 31;
          }
        }
        return 0;
      },
      mayOpen: (node, flags) => {
        if (!node) {
          return 44;
        }
        if ((node.mode & 61440) === 40960) {
          return 32;
        } else if ((node.mode & 61440) === 16384) {
          if (FS.flagsToPermissionString(flags) !== "r" || flags & 512) {
            return 31;
          }
        }
        return FS.nodePermissions(node, FS.flagsToPermissionString(flags));
      },
      MAX_OPEN_FDS: 4096,
      nextfd: () => {
        for (var fd = 0; fd <= 4096; fd++) {
          if (!FS.streams[fd]) {
            return fd;
          }
        }
        throw new null(33);
      },
      getStream: fd => FS.streams[fd],
      createStream: (stream, fd = -1) => {
        if (!FS.FSStream) {
          FS.FSStream = function () {
            this.shared = {};
          };
          FS.FSStream.prototype = {};
          Object.defineProperties(FS.FSStream.prototype, {
            object: {
              get: function () {
                return this.node;
              },
              set: function (val) {
                this.node = val;
              }
            },
            isRead: {
              get: function () {
                return (this.flags & 2097155) !== 1;
              }
            },
            isWrite: {
              get: function () {
                return (this.flags & 2097155) !== 0;
              }
            },
            isAppend: {
              get: function () {
                return this.flags & 1024;
              }
            },
            flags: {
              get: function () {
                return this.shared.flags;
              },
              set: function (val) {
                this.shared.flags = val;
              }
            },
            position: {
              get: function () {
                return this.shared.position;
              },
              set: function (val) {
                this.shared.position = val;
              }
            }
          });
        }
        stream = Object.assign(new FS.FSStream(), stream);
        if (fd == -1) {
          fd = FS.nextfd();
        }
        stream.fd = fd;
        FS.streams[fd] = stream;
        return stream;
      },
      closeStream: fd => {
        FS.streams[fd] = null;
      },
      chrdev_stream_ops: {
        open: stream => {
          var device = FS.devices[stream.node.rdev];
          stream.stream_ops = device.stream_ops;
          if (stream.stream_ops.open) {
            stream.stream_ops.open(stream);
          }
        },
        llseek: () => {
          throw new null(70);
        }
      },
      major: dev => dev >> 8,
      minor: dev => dev & 255,
      makedev: (ma, mi) => ma << 8 | mi,
      registerDevice: (dev, ops) => {
        FS.devices[dev] = {
          stream_ops: ops
        };
      },
      getDevice: dev => FS.devices[dev],
      getMounts: mount => {
        var mounts = [];
        var check = [mount];
        while (check.length) {
          var m = check.pop();
          mounts.push(m);
          check.push.apply(check, m.mounts);
        }
        return mounts;
      },
      syncfs: (populate, callback) => {
        if (typeof populate == "function") {
          callback = populate;
          populate = false;
        }
        0++;
        var mounts = FS.getMounts(null.mount);
        var completed = 0;
        function doCallback(errCode) {
          0--;
          return callback(errCode);
        }
        function done(errCode) {
          if (errCode) {
            if (!done.errored) {
              done.errored = true;
              return doCallback(errCode);
            }
            return;
          }
          if (++completed >= mounts.length) {
            doCallback(null);
          }
        }
        mounts.forEach(mount => {
          if (!mount.type.syncfs) {
            return done(null);
          }
          mount.type.syncfs(mount, populate, done);
        });
      },
      mount: (type, opts, mountpoint) => {
        var root = mountpoint === "/";
        var pseudo = !mountpoint;
        var node;
        if (root && null) {
          throw new null(10);
        } else if (!root && !pseudo) {
          var lookup = FS.lookupPath(mountpoint, {
            follow_mount: false
          });
          mountpoint = lookup.path;
          node = lookup.node;
          if (!!node.mounted) {
            throw new null(10);
          }
          if (!((node.mode & 61440) === 16384)) {
            throw new null(54);
          }
        }
        var mount = {
          type: type,
          opts: opts,
          mountpoint: mountpoint,
          mounts: []
        };
        var mountRoot = type.mount(mount);
        mountRoot.mount = mount;
        mount.root = mountRoot;
        if (root) {
          FS.root = mountRoot;
        } else if (node) {
          node.mounted = mount;
          if (node.mount) {
            node.mount.mounts.push(mount);
          }
        }
        return mountRoot;
      },
      unmount: mountpoint => {
        var lookup = FS.lookupPath(mountpoint, {
          follow_mount: false
        });
        if (!!!lookup.node.mounted) {
          throw new null(28);
        }
        var node = lookup.node;
        var mount = node.mounted;
        var mounts = FS.getMounts(mount);
        Object.keys(null).forEach(hash => {
          var current = null[hash];
          while (current) {
            var next = current.name_next;
            if (mounts.includes(current.mount)) {
              FS.destroyNode(current);
            }
            current = next;
          }
        });
        node.mounted = null;
        var idx = node.mount.mounts.indexOf(mount);
        node.mount.mounts.splice(idx, 1);
      },
      lookup: (parent, name) => {
        return parent.node_ops.lookup(parent, name);
      },
      mknod: (path, mode, dev) => {
        var lookup = FS.lookupPath(path, {
          parent: true
        });
        var parent = lookup.node;
        var name = PATH.basename(path);
        if (!name || name === "." || name === "..") {
          throw new null(28);
        }
        var errCode = FS.mayCreate(parent, name);
        if (errCode) {
          throw new null(errCode);
        }
        if (!parent.node_ops.mknod) {
          throw new null(63);
        }
        return parent.node_ops.mknod(parent, name, mode, dev);
      },
      create: (path, mode) => {
        mode = mode !== undefined ? mode : 438;
        mode &= 4095;
        mode |= 32768;
        return FS.mknod(path, mode, 0);
      },
      mkdir: (path, mode) => {
        mode = mode !== undefined ? mode : 511;
        mode &= 1023;
        mode |= 16384;
        return FS.mknod(path, mode, 0);
      },
      mkdirTree: (path, mode) => {
        var dirs = path.split("/");
        var d = "";
        for (var i = 0; i < dirs.length; ++i) {
          if (!dirs[i]) {
            continue;
          }
          d += "/" + dirs[i];
          try {
            FS.mkdir(d, mode);
          } catch (e) {
            if (e.errno != 20) {
              throw e;
            }
          }
        }
      },
      mkdev: (path, mode, dev) => {
        if (typeof dev == "undefined") {
          dev = mode;
          mode = 438;
        }
        mode |= 8192;
        return FS.mknod(path, mode, dev);
      },
      symlink: (oldpath, newpath) => {
        if (!PATH_FS.resolve(oldpath)) {
          throw new null(44);
        }
        var lookup = FS.lookupPath(newpath, {
          parent: true
        });
        var parent = lookup.node;
        if (!parent) {
          throw new null(44);
        }
        var newname = PATH.basename(newpath);
        var errCode = FS.mayCreate(parent, newname);
        if (errCode) {
          throw new null(errCode);
        }
        if (!parent.node_ops.symlink) {
          throw new null(63);
        }
        return parent.node_ops.symlink(parent, newname, oldpath);
      },
      rename: (old_path, new_path) => {
        var old_dirname = PATH.dirname(old_path);
        var new_dirname = PATH.dirname(new_path);
        var old_name = PATH.basename(old_path);
        var new_name = PATH.basename(new_path);
        var lookup;
        var old_dir;
        var new_dir;
        lookup = FS.lookupPath(old_path, {
          parent: true
        });
        old_dir = lookup.node;
        lookup = FS.lookupPath(new_path, {
          parent: true
        });
        new_dir = lookup.node;
        if (!old_dir || !new_dir) {
          throw new null(44);
        }
        if (old_dir.mount !== new_dir.mount) {
          throw new null(75);
        }
        var old_node = FS.lookupNode(old_dir, old_name);
        var relative = PATH_FS.relative(old_path, new_dirname);
        if (relative.charAt(0) !== ".") {
          throw new null(28);
        }
        relative = PATH_FS.relative(new_path, old_dirname);
        if (relative.charAt(0) !== ".") {
          throw new null(55);
        }
        var new_node;
        try {
          new_node = FS.lookupNode(new_dir, new_name);
        } catch (e) {}
        if (old_node === new_node) {
          return;
        }
        var isdir = (old_node.mode & 61440) === 16384;
        var errCode = FS.mayDelete(old_dir, old_name, isdir);
        if (errCode) {
          throw new null(errCode);
        }
        errCode = new_node ? FS.mayDelete(new_dir, new_name, isdir) : FS.mayCreate(new_dir, new_name);
        if (errCode) {
          throw new null(errCode);
        }
        if (!old_dir.node_ops.rename) {
          throw new null(63);
        }
        if (!!old_node.mounted || new_node && !!new_node.mounted) {
          throw new null(10);
        }
        if (new_dir !== old_dir) {
          errCode = FS.nodePermissions(old_dir, "w");
          if (errCode) {
            throw new null(errCode);
          }
        }
        FS.hashRemoveNode(old_node);
        try {
          old_dir.node_ops.rename(old_node, new_dir, new_name);
        } catch (e) {
          throw e;
        } finally {
          FS.hashAddNode(old_node);
        }
      },
      rmdir: path => {
        var lookup = FS.lookupPath(path, {
          parent: true
        });
        var parent = lookup.node;
        var name = PATH.basename(path);
        var node = FS.lookupNode(parent, name);
        var errCode = FS.mayDelete(parent, name, true);
        if (errCode) {
          throw new null(errCode);
        }
        if (!parent.node_ops.rmdir) {
          throw new null(63);
        }
        if (!!node.mounted) {
          throw new null(10);
        }
        parent.node_ops.rmdir(parent, name);
        FS.destroyNode(node);
      },
      readdir: path => {
        var lookup = FS.lookupPath(path, {
          follow: true
        });
        var node = lookup.node;
        if (!node.node_ops.readdir) {
          throw new null(54);
        }
        return node.node_ops.readdir(node);
      },
      unlink: path => {
        var lookup = FS.lookupPath(path, {
          parent: true
        });
        var parent = lookup.node;
        if (!parent) {
          throw new null(44);
        }
        var name = PATH.basename(path);
        var node = FS.lookupNode(parent, name);
        var errCode = FS.mayDelete(parent, name, false);
        if (errCode) {
          throw new null(errCode);
        }
        if (!parent.node_ops.unlink) {
          throw new null(63);
        }
        if (!!node.mounted) {
          throw new null(10);
        }
        parent.node_ops.unlink(parent, name);
        FS.destroyNode(node);
      },
      readlink: path => {
        var lookup = FS.lookupPath(path);
        var link = lookup.node;
        if (!link) {
          throw new null(44);
        }
        if (!link.node_ops.readlink) {
          throw new null(28);
        }
        return PATH_FS.resolve(FS.getPath(link.parent), link.node_ops.readlink(link));
      },
      stat: (path, dontFollow) => {
        var lookup = FS.lookupPath(path, {
          follow: !dontFollow
        });
        var node = lookup.node;
        if (!node) {
          throw new null(44);
        }
        if (!node.node_ops.getattr) {
          throw new null(63);
        }
        return node.node_ops.getattr(node);
      },
      lstat: path => {
        return FS.stat(path, true);
      },
      chmod: (path, mode, dontFollow) => {
        var node;
        if (typeof path == "string") {
          var lookup = FS.lookupPath(path, {
            follow: !dontFollow
          });
          node = lookup.node;
        } else {
          node = path;
        }
        if (!node.node_ops.setattr) {
          throw new null(63);
        }
        node.node_ops.setattr(node, {
          mode: mode & 4095 | node.mode & -4096,
          timestamp: Date.now()
        });
      },
      lchmod: (path, mode) => {
        FS.chmod(path, mode, true);
      },
      fchmod: (fd, mode) => {
        var stream = FS.streams[fd];
        if (!stream) {
          throw new null(8);
        }
        FS.chmod(stream.node, mode);
      },
      chown: (path, uid, gid, dontFollow) => {
        var node;
        if (typeof path == "string") {
          var lookup = FS.lookupPath(path, {
            follow: !dontFollow
          });
          node = lookup.node;
        } else {
          node = path;
        }
        if (!node.node_ops.setattr) {
          throw new null(63);
        }
        node.node_ops.setattr(node, {
          timestamp: Date.now()
        });
      },
      lchown: (path, uid, gid) => {
        FS.chown(path, uid, gid, true);
      },
      fchown: (fd, uid, gid) => {
        var stream = FS.streams[fd];
        if (!stream) {
          throw new null(8);
        }
        FS.chown(stream.node, uid, gid);
      },
      truncate: (path, len) => {
        if (len < 0) {
          throw new null(28);
        }
        var node;
        if (typeof path == "string") {
          var lookup = FS.lookupPath(path, {
            follow: true
          });
          node = lookup.node;
        } else {
          node = path;
        }
        if (!node.node_ops.setattr) {
          throw new null(63);
        }
        if ((node.mode & 61440) === 16384) {
          throw new null(31);
        }
        if (!((node.mode & 61440) === 32768)) {
          throw new null(28);
        }
        var errCode = FS.nodePermissions(node, "w");
        if (errCode) {
          throw new null(errCode);
        }
        node.node_ops.setattr(node, {
          size: len,
          timestamp: Date.now()
        });
      },
      ftruncate: (fd, len) => {
        var stream = FS.streams[fd];
        if (!stream) {
          throw new null(8);
        }
        if ((stream.flags & 2097155) === 0) {
          throw new null(28);
        }
        FS.truncate(stream.node, len);
      },
      utime: (path, atime, mtime) => {
        var lookup = FS.lookupPath(path, {
          follow: true
        });
        var node = lookup.node;
        node.node_ops.setattr(node, {
          timestamp: Math.max(atime, mtime)
        });
      },
      open: (path, flags, mode) => {
        if (path === "") {
          throw new null(44);
        }
        flags = typeof flags == "string" ? FS_modeStringToFlags(flags) : flags;
        mode = typeof mode == "undefined" ? 438 : mode;
        if (flags & 64) {
          mode = mode & 4095 | 32768;
        } else {
          mode = 0;
        }
        var node;
        if (typeof path == "object") {
          node = path;
        } else {
          path = PATH.normalize(path);
          try {
            var lookup = FS.lookupPath(path, {
              follow: !(flags & 131072)
            });
            node = lookup.node;
          } catch (e) {}
        }
        var created = false;
        if (flags & 64) {
          if (node) {
            if (flags & 128) {
              throw new null(20);
            }
          } else {
            node = FS.mknod(path, mode, 0);
            created = true;
          }
        }
        if (!node) {
          throw new null(44);
        }
        if ((node.mode & 61440) === 8192) {
          flags &= -513;
        }
        if (flags & 65536 && !((node.mode & 61440) === 16384)) {
          throw new null(54);
        }
        if (!created) {
          var errCode = FS.mayOpen(node, flags);
          if (errCode) {
            throw new null(errCode);
          }
        }
        if (flags & 512 && !created) {
          FS.truncate(node, 0);
        }
        flags &= -131713;
        var stream = FS.createStream({
          node: node,
          path: FS.getPath(node),
          flags: flags,
          seekable: true,
          position: 0,
          stream_ops: node.stream_ops,
          ungotten: [],
          error: false
        });
        if (stream.stream_ops.open) {
          stream.stream_ops.open(stream);
        }
        if (Module.logReadFiles && !(flags & 1)) {
          if (!FS.readFiles) {
            FS.readFiles = {};
          }
          if (!(path in FS.readFiles)) {
            FS.readFiles[path] = 1;
          }
        }
        return stream;
      },
      close: stream => {
        if (stream.fd === null) {
          throw new null(8);
        }
        if (stream.getdents) {
          stream.getdents = null;
        }
        try {
          if (stream.stream_ops.close) {
            stream.stream_ops.close(stream);
          }
        } catch (e) {
          throw e;
        } finally {
          FS.closeStream(stream.fd);
        }
        stream.fd = null;
      },
      isClosed: stream => {
        return stream.fd === null;
      },
      llseek: (stream, offset, whence) => {
        if (stream.fd === null) {
          throw new null(8);
        }
        if (!stream.seekable || !stream.stream_ops.llseek) {
          throw new null(70);
        }
        if (whence != 0 && whence != 1 && whence != 2) {
          throw new null(28);
        }
        stream.position = stream.stream_ops.llseek(stream, offset, whence);
        stream.ungotten = [];
        return stream.position;
      },
      read: (stream, buffer, offset, length, position) => {
        if (length < 0 || position < 0) {
          throw new null(28);
        }
        if (stream.fd === null) {
          throw new null(8);
        }
        if ((stream.flags & 2097155) === 1) {
          throw new null(8);
        }
        if ((stream.node.mode & 61440) === 16384) {
          throw new null(31);
        }
        if (!stream.stream_ops.read) {
          throw new null(28);
        }
        var seeking = typeof position != "undefined";
        if (!seeking) {
          position = stream.position;
        } else if (!stream.seekable) {
          throw new null(70);
        }
        var bytesRead = stream.stream_ops.read(stream, buffer, offset, length, position);
        if (!seeking) {
          stream.position += bytesRead;
        }
        return bytesRead;
      },
      write: (stream, buffer, offset, length, position, canOwn) => {
        if (length < 0 || position < 0) {
          throw new null(28);
        }
        if (stream.fd === null) {
          throw new null(8);
        }
        if ((stream.flags & 2097155) === 0) {
          throw new null(8);
        }
        if ((stream.node.mode & 61440) === 16384) {
          throw new null(31);
        }
        if (!stream.stream_ops.write) {
          throw new null(28);
        }
        if (stream.seekable && stream.flags & 1024) {
          FS.llseek(stream, 0, 2);
        }
        var seeking = typeof position != "undefined";
        if (!seeking) {
          position = stream.position;
        } else if (!stream.seekable) {
          throw new null(70);
        }
        var bytesWritten = stream.stream_ops.write(stream, buffer, offset, length, position, canOwn);
        if (!seeking) {
          stream.position += bytesWritten;
        }
        return bytesWritten;
      },
      allocate: (stream, offset, length) => {
        if (stream.fd === null) {
          throw new null(8);
        }
        if (offset < 0 || length <= 0) {
          throw new null(28);
        }
        if ((stream.flags & 2097155) === 0) {
          throw new null(8);
        }
        if (!((stream.node.mode & 61440) === 32768) && !((stream.node.mode & 61440) === 16384)) {
          throw new null(43);
        }
        if (!stream.stream_ops.allocate) {
          throw new null(138);
        }
        stream.stream_ops.allocate(stream, offset, length);
      },
      mmap: (stream, length, position, prot, flags) => {
        if ((prot & 2) !== 0 && (flags & 2) === 0 && (stream.flags & 2097155) !== 2) {
          throw new null(2);
        }
        if ((stream.flags & 2097155) === 1) {
          throw new null(2);
        }
        if (!stream.stream_ops.mmap) {
          throw new null(43);
        }
        return stream.stream_ops.mmap(stream, length, position, prot, flags);
      },
      msync: (stream, buffer, offset, length, mmapFlags) => {
        if (!stream.stream_ops.msync) {
          return 0;
        }
        return stream.stream_ops.msync(stream, buffer, offset, length, mmapFlags);
      },
      munmap: stream => 0,
      ioctl: (stream, cmd, arg) => {
        if (!stream.stream_ops.ioctl) {
          throw new null(59);
        }
        return stream.stream_ops.ioctl(stream, cmd, arg);
      },
      readFile: (path, opts = {}) => {
        opts.flags = opts.flags || 0;
        opts.encoding = opts.encoding || "binary";
        if (opts.encoding !== "utf8" && opts.encoding !== "binary") {
          throw new Error(`Invalid encoding type "${opts.encoding}"`);
        }
        var ret;
        var stream = FS.open(path, opts.flags);
        var stat = FS.stat(path);
        var length = stat.size;
        var buf = new Uint8Array(length);
        FS.read(stream, buf, 0, length, 0);
        if (opts.encoding === "utf8") {
          ret = UTF8ArrayToString(buf, 0);
        } else if (opts.encoding === "binary") {
          ret = buf;
        }
        FS.close(stream);
        return ret;
      },
      writeFile: (path, data, opts = {}) => {
        opts.flags = opts.flags || 577;
        var stream = FS.open(path, opts.flags, opts.mode);
        if (typeof data == "string") {
          var buf = new Uint8Array(lengthBytesUTF8(data) + 1);
          var actualNumBytes = stringToUTF8Array(data, buf, 0, buf.length);
          FS.write(stream, buf, 0, actualNumBytes, undefined, opts.canOwn);
        } else if (ArrayBuffer.isView(data)) {
          FS.write(stream, data, 0, data.byteLength, undefined, opts.canOwn);
        } else {
          throw new Error("Unsupported data type");
        }
        FS.close(stream);
      },
      cwd: () => "/",
      chdir: path => {
        var lookup = FS.lookupPath(path, {
          follow: true
        });
        if (lookup.node === null) {
          throw new null(44);
        }
        if (!((lookup.node.mode & 61440) === 16384)) {
          throw new null(54);
        }
        var errCode = FS.nodePermissions(lookup.node, "x");
        if (errCode) {
          throw new null(errCode);
        }
        FS.currentPath = lookup.path;
      },
      createDefaultDirectories: () => {
        FS.mkdir("/tmp");
        FS.mkdir("/home");
        FS.mkdir("/home/web_user");
      },
      createDefaultDevices: () => {
        FS.mkdir("/dev");
        FS.registerDevice(259, {
          read: () => 0,
          write: (stream, buffer, offset, length, pos) => length
        });
        FS.mkdev("/dev/null", 259);
        TTY.register(1280, TTY.default_tty_ops);
        TTY.register(1536, TTY.default_tty1_ops);
        FS.mkdev("/dev/tty", 1280);
        FS.mkdev("/dev/tty1", 1536);
        var randomBuffer = new Uint8Array(1024);
        var randomLeft = 0;
        var randomByte = () => {
          if (randomLeft === 0) {
            randomLeft = randomFill(randomBuffer).byteLength;
          }
          return randomBuffer[--randomLeft];
        };
        FS.createDevice("/dev", "random", randomByte);
        FS.createDevice("/dev", "urandom", randomByte);
        FS.mkdir("/dev/shm");
        FS.mkdir("/dev/shm/tmp");
      },
      createSpecialDirectories: () => {
        FS.mkdir("/proc");
        var proc_self = FS.mkdir("/proc/self");
        FS.mkdir("/proc/self/fd");
        FS.mount({
          mount: () => {
            var node = FS.createNode(proc_self, "fd", 16895, 73);
            node.node_ops = {
              lookup: (parent, name) => {
                var fd = +name;
                var stream = FS.streams[fd];
                if (!stream) {
                  throw new null(8);
                }
                var ret = {
                  parent: null,
                  mount: {
                    mountpoint: "fake"
                  },
                  node_ops: {
                    readlink: () => stream.path
                  }
                };
                ret.parent = ret;
                return ret;
              }
            };
            return node;
          }
        }, {}, "/proc/self/fd");
      },
      createStandardStreams: () => {
        if (Module.stdin) {
          FS.createDevice("/dev", "stdin", Module.stdin);
        } else {
          FS.symlink("/dev/tty", "/dev/stdin");
        }
        if (Module.stdout) {
          FS.createDevice("/dev", "stdout", null, Module.stdout);
        } else {
          FS.symlink("/dev/tty", "/dev/stdout");
        }
        if (Module.stderr) {
          FS.createDevice("/dev", "stderr", null, Module.stderr);
        } else {
          FS.symlink("/dev/tty1", "/dev/stderr");
        }
      },
      ensureErrnoError: () => {
        return;
        FS.ErrnoError = function ErrnoError(errno, node) {
          this.name = "ErrnoError";
          this.node = node;
          this.setErrno = function (errno) {
            this.errno = errno;
          };
          this.setErrno(errno);
          this.message = "FS error";
        };
        null.prototype = new Error();
        null.prototype.constructor = null;
        [44].forEach(code => {
          FS.genericErrors[code] = new null(code);
          FS.genericErrors[code].stack = "<generic error, no stack>";
        });
      },
      staticInit: () => {
        FS.ensureErrnoError();
        FS.nameTable = new Array(4096);
        FS.mount(MEMFS, {}, "/");
        FS.createDefaultDirectories();
        FS.createDefaultDevices();
        FS.createSpecialDirectories();
        FS.filesystems = {
          "MEMFS": MEMFS,
          "WORKERFS": WORKERFS
        };
      },
      init: (input, output, error) => {
        FS.init.initialized = true;
        FS.ensureErrnoError();
        Module.stdin = input || Module.stdin;
        Module.stdout = output || Module.stdout;
        Module.stderr = error || Module.stderr;
        FS.createStandardStreams();
      },
      quit: () => {
        FS.init.initialized = false;
        for (var i = 0; i < FS.streams.length; i++) {
          var stream = FS.streams[i];
          if (!stream) {
            continue;
          }
          FS.close(stream);
        }
      },
      findObject: (path, dontResolveLastLink) => {
        var ret = FS.analyzePath(path, dontResolveLastLink);
        if (!ret.exists) {
          return null;
        }
        return ret.object;
      },
      analyzePath: (path, dontResolveLastLink) => {
        try {
          var lookup = FS.lookupPath(path, {
            follow: !dontResolveLastLink
          });
          path = lookup.path;
        } catch (e) {}
        var ret = {
          isRoot: false,
          exists: false,
          error: 0,
          name: null,
          path: null,
          object: null,
          parentExists: false,
          parentPath: null,
          parentObject: null
        };
        try {
          var lookup = FS.lookupPath(path, {
            parent: true
          });
          ret.parentExists = true;
          ret.parentPath = lookup.path;
          ret.parentObject = lookup.node;
          ret.name = PATH.basename(path);
          lookup = FS.lookupPath(path, {
            follow: !dontResolveLastLink
          });
          ret.exists = true;
          ret.path = lookup.path;
          ret.object = lookup.node;
          ret.name = lookup.node.name;
          ret.isRoot = lookup.path === "/";
        } catch (e) {
          ret.error = e.errno;
        }
        return ret;
      },
      createPath: (parent, path, canRead, canWrite) => {
        parent = typeof parent == "string" ? parent : FS.getPath(parent);
        var parts = path.split("/").reverse();
        while (parts.length) {
          var part = parts.pop();
          if (!part) {
            continue;
          }
          var current = PATH.normalize(parent + "/" + part);
          try {
            FS.mkdir(current);
          } catch (e) {}
          parent = current;
        }
        return current;
      },
      createFile: (parent, name, properties, canRead, canWrite) => {
        var path = PATH.normalize((typeof parent == "string" ? parent : FS.getPath(parent)) + "/" + name);
        var mode = FS_getMode(canRead, canWrite);
        return FS.create(path, mode);
      },
      createDataFile: (parent, name, data, canRead, canWrite, canOwn) => {
        var path = name;
        if (parent) {
          parent = typeof parent == "string" ? parent : FS.getPath(parent);
          path = name ? PATH.normalize(parent + "/" + name) : parent;
        }
        var mode = FS_getMode(canRead, canWrite);
        var node = FS.create(path, mode);
        if (data) {
          if (typeof data == "string") {
            var arr = new Array(data.length);
            var i = 0;
            for (var len = data.length; i < len; ++i) {
              arr[i] = data.charCodeAt(i);
            }
            data = arr;
          }
          FS.chmod(node, mode | 146);
          var stream = FS.open(node, 577);
          FS.write(stream, data, 0, data.length, 0, canOwn);
          FS.close(stream);
          FS.chmod(node, mode);
        }
        return node;
      },
      createDevice: (parent, name, input, output) => {
        var path = PATH.normalize((typeof parent == "string" ? parent : FS.getPath(parent)) + "/" + name);
        var mode = FS_getMode(!!input, !!output);
        if (!FS.createDevice.major) {
          FS.createDevice.major = 64;
        }
        var dev = FS.createDevice.major++ << 8 | 0;
        FS.registerDevice(dev, {
          open: stream => {
            stream.seekable = false;
          },
          close: stream => {
            if (output && output.buffer && output.buffer.length) {
              output(10);
            }
          },
          read: (stream, buffer, offset, length, pos) => {
            var bytesRead = 0;
            for (var i = 0; i < length; i++) {
              var result;
              try {
                result = input();
              } catch (e) {
                throw new null(29);
              }
              if (result === undefined && bytesRead === 0) {
                throw new null(6);
              }
              if (result === null || result === undefined) {
                break;
              }
              bytesRead++;
              buffer[offset + i] = result;
            }
            if (bytesRead) {
              stream.node.timestamp = Date.now();
            }
            return bytesRead;
          },
          write: (stream, buffer, offset, length, pos) => {
            for (var i = 0; i < length; i++) {
              try {
                output(buffer[offset + i]);
              } catch (e) {
                throw new null(29);
              }
            }
            if (length) {
              stream.node.timestamp = Date.now();
            }
            return i;
          }
        });
        return FS.mkdev(path, mode, dev);
      },
      forceLoadFile: obj => {
        if (obj.isDevice || obj.isFolder || obj.link || obj.contents) {
          return true;
        }
        if (typeof XMLHttpRequest != "undefined") {
          throw new Error("Lazy loading should have been performed (contents set) in createLazyFile, but it was not. Lazy loading only works in web workers. Use --embed-file or --preload-file in emcc on the main thread.");
        } else if (read_) {
          try {
            obj.contents = intArrayFromString(read_(obj.url), true);
            obj.usedBytes = obj.contents.length;
          } catch (e) {
            throw new null(29);
          }
        } else {
          throw new Error("Cannot load without read() or XMLHttpRequest.");
        }
      },
      createLazyFile: (parent, name, url, canRead, canWrite) => {
        function LazyUint8Array() {
          this.lengthKnown = false;
          this.chunks = [];
        }
        LazyUint8Array.prototype.get = function LazyUint8Array_get(idx) {
          if (idx > this.length - 1 || idx < 0) {
            return undefined;
          }
          var chunkOffset = idx % this.chunkSize;
          var chunkNum = idx / this.chunkSize | 0;
          return this.getter(chunkNum)[chunkOffset];
        };
        LazyUint8Array.prototype.setDataGetter = function LazyUint8Array_setDataGetter(getter) {
          this.getter = getter;
        };
        LazyUint8Array.prototype.cacheLength = function LazyUint8Array_cacheLength() {
          var xhr = new XMLHttpRequest();
          xhr.open("HEAD", url, false);
          xhr.send(null);
          if (!(xhr.status >= 200 && xhr.status < 300 || xhr.status === 304)) {
            throw new Error("Couldn't load " + url + ". Status: " + xhr.status);
          }
          var datalength = Number(xhr.getResponseHeader("Content-length"));
          var header;
          var hasByteServing = (header = xhr.getResponseHeader("Accept-Ranges")) && header === "bytes";
          var usesGzip = (header = xhr.getResponseHeader("Content-Encoding")) && header === "gzip";
          var chunkSize = 1048576;
          if (!hasByteServing) {
            chunkSize = datalength;
          }
          var doXHR = (from, to) => {
            if (from > to) {
              throw new Error("invalid range (" + from + ", " + to + ") or no bytes requested!");
            }
            if (to > datalength - 1) {
              throw new Error("only " + datalength + " bytes available! programmer error!");
            }
            var xhr = new XMLHttpRequest();
            xhr.open("GET", url, false);
            if (datalength !== chunkSize) {
              xhr.setRequestHeader("Range", "bytes=" + from + "-" + to);
            }
            xhr.responseType = "arraybuffer";
            if (xhr.overrideMimeType) {
              xhr.overrideMimeType("text/plain; charset=x-user-defined");
            }
            xhr.send(null);
            if (!(xhr.status >= 200 && xhr.status < 300 || xhr.status === 304)) {
              throw new Error("Couldn't load " + url + ". Status: " + xhr.status);
            }
            if (xhr.response !== undefined) {
              return new Uint8Array(xhr.response || []);
            }
            return intArrayFromString(xhr.responseText || "", true);
          };
          var lazyArray = this;
          lazyArray.setDataGetter(chunkNum => {
            var start = chunkNum * chunkSize;
            var end = (chunkNum + 1) * chunkSize - 1;
            end = Math.min(end, datalength - 1);
            if (typeof lazyArray.chunks[chunkNum] == "undefined") {
              lazyArray.chunks[chunkNum] = doXHR(start, end);
            }
            if (typeof lazyArray.chunks[chunkNum] == "undefined") {
              throw new Error("doXHR failed!");
            }
            return lazyArray.chunks[chunkNum];
          });
          if (usesGzip || !datalength) {
            chunkSize = datalength = 1;
            datalength = this.getter(0).length;
            chunkSize = datalength;
            out("LazyFiles on gzip forces download of the whole file when length is accessed");
          }
          this._length = datalength;
          this._chunkSize = chunkSize;
          this.lengthKnown = true;
        };
        if (typeof XMLHttpRequest != "undefined") {
          if (!ENVIRONMENT_IS_WORKER) {
            throw "Cannot do synchronous binary XHRs outside webworkers in modern browsers. Use --embed-file or --preload-file in emcc";
          }
          var lazyArray = new LazyUint8Array();
          Object.defineProperties(lazyArray, {
            length: {
              get: function () {
                if (!this.lengthKnown) {
                  this.cacheLength();
                }
                return this._length;
              }
            },
            chunkSize: {
              get: function () {
                if (!this.lengthKnown) {
                  this.cacheLength();
                }
                return this._chunkSize;
              }
            }
          });
          var properties = {
            isDevice: false,
            contents: lazyArray
          };
        } else {
          var properties = {
            isDevice: false,
            url: url
          };
        }
        var node = FS.createFile(parent, name, properties, canRead, canWrite);
        if (properties.contents) {
          node.contents = properties.contents;
        } else if (properties.url) {
          node.contents = null;
          node.url = properties.url;
        }
        Object.defineProperties(node, {
          usedBytes: {
            get: function () {
              return this.contents.length;
            }
          }
        });
        var stream_ops = {};
        var keys = Object.keys(node.stream_ops);
        keys.forEach(key => {
          var fn = node.stream_ops[key];
          stream_ops[key] = function forceLoadLazyFile() {
            FS.forceLoadFile(node);
            return fn.apply(null, arguments);
          };
        });
        function writeChunks(stream, buffer, offset, length, position) {
          var contents = stream.node.contents;
          if (position >= contents.length) {
            return 0;
          }
          var size = Math.min(contents.length - position, length);
          if (contents.slice) {
            for (var i = 0; i < size; i++) {
              buffer[offset + i] = contents[position + i];
            }
          } else {
            for (var i = 0; i < size; i++) {
              buffer[offset + i] = contents.get(position + i);
            }
          }
          return size;
        }
        stream_ops.read = (stream, buffer, offset, length, position) => {
          FS.forceLoadFile(node);
          return writeChunks(stream, buffer, offset, length, position);
        };
        stream_ops.mmap = (stream, length, position, prot, flags) => {
          FS.forceLoadFile(node);
          var ptr = mmapAlloc(length);
          if (!ptr) {
            throw new null(48);
          }
          writeChunks(stream, HEAP8, ptr, length, position);
          return {
            ptr: ptr,
            allocated: true
          };
        };
        node.stream_ops = stream_ops;
        return node;
      }
    };
    var SYSCALLS = {
      DEFAULT_POLLMASK: 5,
      calculateAt: function (dirfd, path, allowEmpty) {
        if (path.charAt(0) === "/") {
          return path;
        }
        var dir;
        if (dirfd === -100) {
          dir = "/";
        } else {
          var dirstream = SYSCALLS.getStreamFromFD(dirfd);
          dir = dirstream.path;
        }
        if (path.length == 0) {
          if (!allowEmpty) {
            throw new null(44);
          }
          return dir;
        }
        return PATH.normalize(dir + "/" + path);
      },
      doStat: function (func, path, buf) {
        try {
          var stat = func(path);
        } catch (e) {
          if (e && e.node && PATH.normalize(path) !== PATH.normalize(FS.getPath(e.node))) {
            return -54;
          }
          throw e;
        }
        HEAP32[buf >> 2] = stat.dev;
        HEAP32[buf + 8 >> 2] = stat.ino;
        HEAP32[buf + 12 >> 2] = stat.mode;
        HEAPU32[buf + 16 >> 2] = stat.nlink;
        HEAP32[buf + 20 >> 2] = stat.uid;
        HEAP32[buf + 24 >> 2] = stat.gid;
        HEAP32[buf + 28 >> 2] = stat.rdev;
        HEAP64[buf + 40 >> 3] = BigInt(stat.size);
        HEAP32[buf + 48 >> 2] = 4096;
        HEAP32[buf + 52 >> 2] = stat.blocks;
        var atime = stat.atime.getTime();
        var mtime = stat.mtime.getTime();
        var ctime = stat.ctime.getTime();
        HEAP64[buf + 56 >> 3] = BigInt(Math.floor(atime / 1e3));
        HEAPU32[buf + 64 >> 2] = atime % 1e3 * 1e3;
        HEAP64[buf + 72 >> 3] = BigInt(Math.floor(mtime / 1e3));
        HEAPU32[buf + 80 >> 2] = mtime % 1e3 * 1e3;
        HEAP64[buf + 88 >> 3] = BigInt(Math.floor(ctime / 1e3));
        HEAPU32[buf + 96 >> 2] = ctime % 1e3 * 1e3;
        HEAP64[buf + 104 >> 3] = BigInt(stat.ino);
        return 0;
      },
      doMsync: function (addr, stream, len, flags, offset) {
        if (!((stream.node.mode & 61440) === 32768)) {
          throw new null(43);
        }
        if (flags & 2) {
          return 0;
        }
        var buffer = HEAPU8.slice(addr, addr + len);
        FS.msync(stream, buffer, offset, len, flags);
      },
      varargs: undefined,
      get: function () {
        SYSCALLS.varargs += 4;
        var ret = HEAP32[SYSCALLS.varargs - 4 >> 2];
        return ret;
      },
      getStr: function (ptr) {
        var ret = ptr ? UTF8ArrayToString(HEAPU8, ptr, undefined) : "";
        return ret;
      },
      getStreamFromFD: function (fd) {
        var stream = FS.streams[fd];
        if (!stream) {
          throw new null(8);
        }
        return stream;
      }
    };
    var SOCKFS = {
      mount: function (mount) {
        Module.websocket = Module.websocket && "object" === typeof Module.websocket ? Module.websocket : {};
        Module.websocket._callbacks = {};
        Module.websocket.on = function (event, callback) {
          if ("function" === typeof callback) {
            this._callbacks[event] = callback;
          }
          return this;
        };
        Module.websocket.emit = function (event, param) {
          if ("function" === typeof this._callbacks[event]) {
            this._callbacks[event].call(this, param);
          }
        };
        return FS.createNode(null, "/", 16895, 0);
      },
      createSocket: function (family, type, protocol) {
        type &= -526337;
        var streaming = type == 1;
        if (streaming && protocol && protocol != 6) {
          throw new null(66);
        }
        var sock = {
          family: family,
          type: type,
          protocol: protocol,
          server: null,
          error: null,
          peers: {},
          pending: [],
          recv_queue: [],
          sock_ops: SOCKFS.websocket_sock_ops
        };
        var name = SOCKFS.nextname();
        var node = FS.createNode(SOCKFS.root, name, 49152, 0);
        node.sock = sock;
        var stream = FS.createStream({
          path: name,
          node: node,
          flags: 2,
          seekable: false,
          stream_ops: SOCKFS.stream_ops
        });
        sock.stream = stream;
        return sock;
      },
      getSocket: function (fd) {
        var stream = FS.streams[fd];
        if (!stream || !((stream.node.mode & 49152) === 49152)) {
          return null;
        }
        return stream.node.sock;
      },
      stream_ops: {
        poll: function (stream) {
          var sock = stream.node.sock;
          return sock.sock_ops.poll(sock);
        },
        ioctl: function (stream, request, varargs) {
          var sock = stream.node.sock;
          return sock.sock_ops.ioctl(sock, request, varargs);
        },
        read: function (stream, buffer, offset, length, position) {
          var sock = stream.node.sock;
          var msg = sock.sock_ops.recvmsg(sock, length);
          if (!msg) {
            return 0;
          }
          buffer.set(msg.buffer, offset);
          return msg.buffer.length;
        },
        write: function (stream, buffer, offset, length, position) {
          var sock = stream.node.sock;
          return sock.sock_ops.sendmsg(sock, buffer, offset, length);
        },
        close: function (stream) {
          var sock = stream.node.sock;
          sock.sock_ops.close(sock);
        }
      },
      nextname: function () {
        if (!SOCKFS.nextname.current) {
          SOCKFS.nextname.current = 0;
        }
        return "socket[" + SOCKFS.nextname.current++ + "]";
      },
      websocket_sock_ops: {
        createPeer: function (sock, addr, port) {
          var ws;
          if (typeof addr == "object") {
            ws = addr;
            addr = null;
            port = null;
          }
          if (ws) {
            if (ws._socket) {
              addr = ws._socket.remoteAddress;
              port = ws._socket.remotePort;
            } else {
              var result = /ws[s]?:\/\/([^:]+):(\d+)/.exec(ws.url);
              if (!result) {
                throw new Error("WebSocket URL must be in the format ws(s)://address:port");
              }
              addr = result[1];
              port = parseInt(result[2], 10);
            }
          } else {
            try {
              var runtimeConfig = Module.websocket && "object" === typeof Module.websocket;
              var url = "ws:#".replace("#", "//");
              if (runtimeConfig) {
                if ("string" === typeof Module.websocket.url) {
                  url = Module.websocket.url;
                }
              }
              if (url === "ws://" || url === "wss://") {
                var parts = addr.split("/");
                url = url + parts[0] + ":" + port + "/" + parts.slice(1).join("/");
              }
              var subProtocols = "binary";
              if (runtimeConfig) {
                if ("string" === typeof Module.websocket.subprotocol) {
                  subProtocols = Module.websocket.subprotocol;
                }
              }
              var opts = undefined;
              if (subProtocols !== "null") {
                subProtocols = subProtocols.replace(/^ +| +$/g, "").split(/ *, */);
                opts = subProtocols;
              }
              if (runtimeConfig && null === Module.websocket.subprotocol) {
                subProtocols = "null";
                opts = undefined;
              }
              var WebSocketConstructor;
              if (ENVIRONMENT_IS_NODE) {
                WebSocketConstructor = require("ws");
              } else {
                WebSocketConstructor = WebSocket;
              }
              ws = new WebSocketConstructor(url, opts);
              ws.binaryType = "arraybuffer";
            } catch (e) {
              throw new null(23);
            }
          }
          var peer = {
            addr: addr,
            port: port,
            socket: ws,
            dgram_send_queue: []
          };
          SOCKFS.websocket_sock_ops.addPeer(sock, peer);
          SOCKFS.websocket_sock_ops.handlePeerEvents(sock, peer);
          if (sock.type === 2 && typeof sock.sport != "undefined") {
            peer.dgram_send_queue.push(new Uint8Array([255, 255, 255, 255, "p".charCodeAt(0), "o".charCodeAt(0), "r".charCodeAt(0), "t".charCodeAt(0), (sock.sport & 65280) >> 8, sock.sport & 255]));
          }
          return peer;
        },
        getPeer: function (sock, addr, port) {
          return sock.peers[addr + ":" + port];
        },
        addPeer: function (sock, peer) {
          sock.peers[peer.addr + ":" + peer.port] = peer;
        },
        removePeer: function (sock, peer) {
          delete sock.peers[peer.addr + ":" + peer.port];
        },
        handlePeerEvents: function (sock, peer) {
          var first = true;
          var handleOpen = function () {
            Module.websocket.emit("open", sock.stream.fd);
            try {
              var queued = peer.dgram_send_queue.shift();
              while (queued) {
                peer.socket.send(queued);
                queued = peer.dgram_send_queue.shift();
              }
            } catch (e) {
              peer.socket.close();
            }
          };
          function handleMessage(data) {
            if (typeof data == "string") {
              var encoder = new TextEncoder();
              data = encoder.encode(data);
            } else {
              assert(data.byteLength !== undefined);
              if (data.byteLength == 0) {
                return;
              }
              data = new Uint8Array(data);
            }
            var wasfirst = first;
            first = false;
            if (wasfirst && data.length === 10 && data[0] === 255 && data[1] === 255 && data[2] === 255 && data[3] === 255 && data[4] === "p".charCodeAt(0) && data[5] === "o".charCodeAt(0) && data[6] === "r".charCodeAt(0) && data[7] === "t".charCodeAt(0)) {
              var newport = data[8] << 8 | data[9];
              SOCKFS.websocket_sock_ops.removePeer(sock, peer);
              peer.port = newport;
              SOCKFS.websocket_sock_ops.addPeer(sock, peer);
              return;
            }
            sock.recv_queue.push({
              addr: peer.addr,
              port: peer.port,
              data: data
            });
            Module.websocket.emit("message", sock.stream.fd);
          }
          if (ENVIRONMENT_IS_NODE) {
            peer.socket.on("open", handleOpen);
            peer.socket.on("message", function (data, isBinary) {
              if (!isBinary) {
                return;
              }
              handleMessage(new Uint8Array(data).buffer);
            });
            peer.socket.on("close", function () {
              Module.websocket.emit("close", sock.stream.fd);
            });
            peer.socket.on("error", function (error) {
              sock.error = 14;
              Module.websocket.emit("error", [sock.stream.fd, sock.error, "ECONNREFUSED: Connection refused"]);
            });
          } else {
            peer.socket.onopen = handleOpen;
            peer.socket.onclose = function () {
              Module.websocket.emit("close", sock.stream.fd);
            };
            peer.socket.onmessage = function peer_socket_onmessage(event) {
              handleMessage(event.data);
            };
            peer.socket.onerror = function (error) {
              sock.error = 14;
              Module.websocket.emit("error", [sock.stream.fd, sock.error, "ECONNREFUSED: Connection refused"]);
            };
          }
        },
        poll: function (sock) {
          if (sock.type === 1 && sock.server) {
            return sock.pending.length ? 65 : 0;
          }
          var mask = 0;
          var dest = sock.type === 1 ? SOCKFS.websocket_sock_ops.getPeer(sock, sock.daddr, sock.dport) : null;
          if (sock.recv_queue.length || !dest || dest && dest.socket.readyState === dest.socket.CLOSING || dest && dest.socket.readyState === dest.socket.CLOSED) {
            mask |= 65;
          }
          if (!dest || dest && dest.socket.readyState === dest.socket.OPEN) {
            mask |= 4;
          }
          if (dest && dest.socket.readyState === dest.socket.CLOSING || dest && dest.socket.readyState === dest.socket.CLOSED) {
            mask |= 16;
          }
          return mask;
        },
        ioctl: function (sock, request, arg) {
          switch (request) {
            case 21531:
              var bytes = 0;
              if (sock.recv_queue.length) {
                bytes = sock.recv_queue[0].data.length;
              }
              HEAP32[arg >> 2] = bytes;
              return 0;
            default:
              return 28;
          }
        },
        close: function (sock) {
          if (sock.server) {
            try {
              sock.server.close();
            } catch (e) {}
            sock.server = null;
          }
          var peers = Object.keys(sock.peers);
          for (var i = 0; i < peers.length; i++) {
            var peer = sock.peers[peers[i]];
            try {
              peer.socket.close();
            } catch (e) {}
            SOCKFS.websocket_sock_ops.removePeer(sock, peer);
          }
          return 0;
        },
        bind: function (sock, addr, port) {
          if (typeof sock.saddr != "undefined" || typeof sock.sport != "undefined") {
            throw new null(28);
          }
          sock.saddr = addr;
          sock.sport = port;
          if (sock.type === 2) {
            if (sock.server) {
              sock.server.close();
              sock.server = null;
            }
            try {
              sock.sock_ops.listen(sock, 0);
            } catch (e) {
              if (!(e.name === "ErrnoError")) {
                throw e;
              }
              if (e.errno !== 138) {
                throw e;
              }
            }
          }
        },
        connect: function (sock, addr, port) {
          if (sock.server) {
            throw new null(138);
          }
          if (typeof sock.daddr != "undefined" && typeof sock.dport != "undefined") {
            var dest = SOCKFS.websocket_sock_ops.getPeer(sock, sock.daddr, sock.dport);
            if (dest) {
              if (dest.socket.readyState === dest.socket.CONNECTING) {
                throw new null(7);
              } else {
                throw new null(30);
              }
            }
          }
          var peer = SOCKFS.websocket_sock_ops.createPeer(sock, addr, port);
          sock.daddr = peer.addr;
          sock.dport = peer.port;
          throw new null(26);
        },
        listen: function (sock, backlog) {
          if (!ENVIRONMENT_IS_NODE) {
            throw new null(138);
          }
          if (sock.server) {
            throw new null(28);
          }
          var WebSocketServer = require("ws").Server;
          var host = sock.saddr;
          sock.server = new WebSocketServer({
            host: host,
            port: sock.sport
          });
          Module.websocket.emit("listen", sock.stream.fd);
          sock.server.on("connection", function (ws) {
            if (sock.type === 1) {
              var newsock = SOCKFS.createSocket(sock.family, sock.type, sock.protocol);
              var peer = SOCKFS.websocket_sock_ops.createPeer(newsock, ws);
              newsock.daddr = peer.addr;
              newsock.dport = peer.port;
              sock.pending.push(newsock);
              Module.websocket.emit("connection", newsock.stream.fd);
            } else {
              SOCKFS.websocket_sock_ops.createPeer(sock, ws);
              Module.websocket.emit("connection", sock.stream.fd);
            }
          });
          sock.server.on("close", function () {
            Module.websocket.emit("close", sock.stream.fd);
            sock.server = null;
          });
          sock.server.on("error", function (error) {
            sock.error = 23;
            Module.websocket.emit("error", [sock.stream.fd, sock.error, "EHOSTUNREACH: Host is unreachable"]);
          });
        },
        accept: function (listensock) {
          if (!listensock.server || !listensock.pending.length) {
            throw new null(28);
          }
          var newsock = listensock.pending.shift();
          newsock.stream.flags = listensock.stream.flags;
          return newsock;
        },
        getname: function (sock, peer) {
          var addr;
          var port;
          if (peer) {
            if (sock.daddr === undefined || sock.dport === undefined) {
              throw new null(53);
            }
            addr = sock.daddr;
            port = sock.dport;
          } else {
            addr = sock.saddr || 0;
            port = sock.sport || 0;
          }
          return {
            addr: addr,
            port: port
          };
        },
        sendmsg: function (sock, buffer, offset, length, addr, port) {
          if (sock.type === 2) {
            if (addr === undefined || port === undefined) {
              addr = sock.daddr;
              port = sock.dport;
            }
            if (addr === undefined || port === undefined) {
              throw new null(17);
            }
          } else {
            addr = sock.daddr;
            port = sock.dport;
          }
          var dest = SOCKFS.websocket_sock_ops.getPeer(sock, addr, port);
          if (sock.type === 1) {
            if (!dest || dest.socket.readyState === dest.socket.CLOSING || dest.socket.readyState === dest.socket.CLOSED) {
              throw new null(53);
            } else if (dest.socket.readyState === dest.socket.CONNECTING) {
              throw new null(6);
            }
          }
          if (ArrayBuffer.isView(buffer)) {
            offset += buffer.byteOffset;
            buffer = buffer.buffer;
          }
          var data;
          data = buffer.slice(offset, offset + length);
          if (sock.type === 2) {
            if (!dest || dest.socket.readyState !== dest.socket.OPEN) {
              if (!dest || dest.socket.readyState === dest.socket.CLOSING || dest.socket.readyState === dest.socket.CLOSED) {
                dest = SOCKFS.websocket_sock_ops.createPeer(sock, addr, port);
              }
              dest.dgram_send_queue.push(data);
              return length;
            }
          }
          try {
            dest.socket.send(data);
            return length;
          } catch (e) {
            throw new null(28);
          }
        },
        recvmsg: function (sock, length) {
          if (sock.type === 1 && sock.server) {
            throw new null(53);
          }
          var queued = sock.recv_queue.shift();
          if (!queued) {
            if (sock.type === 1) {
              var dest = SOCKFS.websocket_sock_ops.getPeer(sock, sock.daddr, sock.dport);
              if (!dest) {
                throw new null(53);
              }
              if (dest.socket.readyState === dest.socket.CLOSING || dest.socket.readyState === dest.socket.CLOSED) {
                return null;
              }
              throw new null(6);
            }
            throw new null(6);
          }
          var queuedLength = queued.data.byteLength || queued.data.length;
          var queuedOffset = queued.data.byteOffset || 0;
          var queuedBuffer = queued.data.buffer || queued.data;
          var bytesRead = Math.min(length, queuedLength);
          var res = {
            buffer: new Uint8Array(queuedBuffer, queuedOffset, bytesRead),
            addr: queued.addr,
            port: queued.port
          };
          if (sock.type === 1 && bytesRead < queuedLength) {
            var bytesRemaining = queuedLength - bytesRead;
            queued.data = new Uint8Array(queuedBuffer, queuedOffset + bytesRead, bytesRemaining);
            sock.recv_queue.unshift(queued);
          }
          return res;
        }
      }
    };
    function inetPton4(str) {
      var b = str.split(".");
      for (var i = 0; i < 4; i++) {
        var tmp = Number(b[i]);
        if (isNaN(tmp)) {
          return null;
        }
        b[i] = tmp;
      }
      return (b[0] | b[1] << 8 | b[2] << 16 | b[3] << 24) >>> 0;
    }
    function inetPton6(str) {
      var words;
      var w;
      var offset;
      var z;
      var valid6regx = /^((?=.*::)(?!.*::.+::)(::)?([\dA-F]{1,4}:(:|\b)|){5}|([\dA-F]{1,4}:){6})((([\dA-F]{1,4}((?!\3)::|:\b|$))|(?!\2\3)){2}|(((2[0-4]|1\d|[1-9])?\d|25[0-5])\.?\b){4})$/i;
      var parts = [];
      if (!valid6regx.test(str)) {
        return null;
      }
      if (str === "::") {
        return [0, 0, 0, 0, 0, 0, 0, 0];
      }
      if (str.startsWith("::")) {
        str = str.replace("::", "Z:");
      } else {
        str = str.replace("::", ":Z:");
      }
      if (str.indexOf(".") > 0) {
        str = str.replace(new RegExp("[.]", "g"), ":");
        words = str.split(":");
        words[words.length - 4] = parseInt(words[words.length - 4]) + parseInt(words[words.length - 3]) * 256;
        words[words.length - 3] = parseInt(words[words.length - 2]) + parseInt(words[words.length - 1]) * 256;
        words = words.slice(0, words.length - 2);
      } else {
        words = str.split(":");
      }
      offset = 0;
      z = 0;
      for (w = 0; w < words.length; w++) {
        if (typeof words[w] == "string") {
          if (words[w] === "Z") {
            for (z = 0; z < 8 - words.length + 1; z++) {
              parts[w + z] = 0;
            }
            offset = z - 1;
          } else {
            parts[w + offset] = _htons(parseInt(words[w], 16));
          }
        } else {
          parts[w + offset] = words[w];
        }
      }
      return [parts[1] << 16 | parts[0], parts[3] << 16 | parts[2], parts[5] << 16 | parts[4], parts[7] << 16 | parts[6]];
    }
    var DNS = {
      address_map: {
        id: 1,
        addrs: {},
        names: {}
      },
      lookup_name: function (name) {
        var res = inetPton4(name);
        if (res !== null) {
          return name;
        }
        res = inetPton6(name);
        if (res !== null) {
          return name;
        }
        var addr;
        if (DNS.address_map.addrs[name]) {
          addr = DNS.address_map.addrs[name];
        } else {
          var id = DNS.address_map.id++;
          assert(id < 65535, "exceeded max address mappings of 65535");
          addr = "172.29." + (id & 255) + "." + (id & 65280);
          DNS.address_map.names[addr] = name;
          DNS.address_map.addrs[name] = addr;
        }
        return addr;
      },
      lookup_addr: function (addr) {
        if (DNS.address_map.names[addr]) {
          return DNS.address_map.names[addr];
        }
        return null;
      }
    };
    function stringToUTF8(str, outPtr, maxBytesToWrite) {
      return stringToUTF8Array(str, HEAPU8, outPtr, maxBytesToWrite);
    }
    function _abort() {
      abort("");
    }
    Module._abort = _abort;
    var _emscripten_get_now;
    if (ENVIRONMENT_IS_NODE) {
      global.performance = require("perf_hooks").performance;
    }
    _emscripten_get_now = () => performance.now();
    var ENV = {};
    function getEnvStrings() {
      if (!getEnvStrings.strings) {
        var lang = (typeof navigator == "object" && navigator.languages && navigator.languages[0] || "C").replace("-", "_") + ".UTF-8";
        var env = {
          "USER": "web_user",
          "LOGNAME": "web_user",
          "PATH": "/",
          "PWD": "/",
          "HOME": "/home/web_user",
          "LANG": lang,
          "_": thisProgram || "./this.program"
        };
        for (var x in ENV) {
          if (ENV[x] === undefined) {
            delete env[x];
          } else {
            env[x] = ENV[x];
          }
        }
        var strings = [];
        for (var x in env) {
          strings.push(`${x}=${env[x]}`);
        }
        getEnvStrings.strings = strings;
      }
      return getEnvStrings.strings;
    }
    var FSNode = function (parent, name, mode, rdev) {
      if (!parent) {
        parent = this;
      }
      this.parent = parent;
      this.mount = parent.mount;
      this.mounted = null;
      this.id = 1++;
      this.name = name;
      this.mode = mode;
      this.node_ops = {};
      this.stream_ops = {};
      this.rdev = rdev;
    };
    Object.defineProperties(FSNode.prototype, {
      read: {
        get: function () {
          return (this.mode & 365) === 365;
        },
        set: function (val) {
          if (val) {
            this.mode |= 365;
          } else {
            this.mode &= -366;
          }
        }
      },
      write: {
        get: function () {
          return (this.mode & 146) === 146;
        },
        set: function (val) {
          if (val) {
            this.mode |= 146;
          } else {
            this.mode &= -147;
          }
        }
      },
      isFolder: {
        get: function () {
          return (this.mode & 61440) === 16384;
        }
      },
      isDevice: {
        get: function () {
          return (this.mode & 61440) === 8192;
        }
      }
    });
    FS.FSNode = FSNode;
    FS.createPreloadedFile = FS_createPreloadedFile;
    FS.staticInit();
    var ___wasm_call_ctors = function () {
      return (___wasm_call_ctors = Module.asm.sa).apply(null, arguments);
    };
    var _malloc = Module._malloc = function () {
      return (_malloc = Module._malloc = Module.asm.ta).apply(null, arguments);
    };
    var ___errno_location = function () {
      return (___errno_location = Module.asm.va).apply(null, arguments);
    };
    var _ntohs = function () {
      return (_ntohs = Module.asm.wa).apply(null, arguments);
    };
    var _htons = function () {
      return (_htons = Module.asm.xa).apply(null, arguments);
    };
    var _ffmpeg = Module._ffmpeg = function () {
      return (_ffmpeg = Module._ffmpeg = Module.asm.ya).apply(null, arguments);
    };
    var _htonl = function () {
      return (_htonl = Module.asm.za).apply(null, arguments);
    };
    var _emscripten_builtin_memalign = function () {
      return (_emscripten_builtin_memalign = Module.asm.Aa).apply(null, arguments);
    };
    var _setThrew = function () {
      return (_setThrew = Module.asm.Ba).apply(null, arguments);
    };
    var stackSave = function () {
      return (stackSave = Module.asm.Ca).apply(null, arguments);
    };
    var stackRestore = function () {
      return (stackRestore = Module.asm.Da).apply(null, arguments);
    };
    var ___cxa_is_pointer_type = function () {
      return (___cxa_is_pointer_type = Module.asm.Ea).apply(null, arguments);
    };
    Module.setValue = setValue;
    Module.getValue = getValue;
    Module.UTF8ToString = UTF8ToString;
    Module.stringToUTF8 = stringToUTF8;
    Module.lengthBytesUTF8 = lengthBytesUTF8;
    Module.FS = FS;
    var calledRun;
    dependenciesFulfilled = function runCaller() {
      if (!calledRun) {
        run();
      }
      if (!calledRun) {
        dependenciesFulfilled = runCaller;
      }
    };
    function run() {
      if (runDependencies > 0) {
        return;
      }
      preRun();
      if (runDependencies > 0) {
        return;
      }
      function doRun() {
        if (calledRun) {
          return;
        }
        calledRun = true;
        Module.calledRun = true;
        if (ABORT) {
          return;
        }
        initRuntime();
        readyPromiseResolve(Module);
        if (Module.onRuntimeInitialized) {
          Module.onRuntimeInitialized();
        }
        postRun();
      }
      if (Module.setStatus) {
        Module.setStatus("Running...");
        setTimeout(function () {
          setTimeout(function () {
            Module.setStatus("");
          }, 1);
          doRun();
        }, 1);
      } else {
        doRun();
      }
    }
    if (Module.preInit) {
      if (typeof Module.preInit == "function") {
        Module.preInit = [Module.preInit];
      }
      while (Module.preInit.length > 0) {
        Module.preInit.pop()();
      }
    }
    run();
    return createFFmpegCore.ready;
  };
})();
export default createFFmpegCore;
```
