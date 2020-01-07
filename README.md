# GenericEfc
Métodos genéricos para sumar, restar y multiplicar (int, double, float)

protocol OperacionesBasicas {
    static func +(op1: Self, op2: Self) -> Self
    static func -(op1: Self, op2: Self) -> Self
    static func *(op1: Self, op2: Self) -> Self
}

extension Double: OperacionesBasicas {}
extension Float: OperacionesBasicas {}
extension Int: OperacionesBasicas {}

func operacionSuma<T: Numeric>(op1: T, op2: T) -> T {
    return op1 + op2
}

func operacionResta<T: Numeric>(op1: T, op2: T) -> T {
    return op1 - op2
}

func operacionMultiplicar<T: Numeric>(op1: T, op2: T) -> T {
    return op1 * op2
}

operacionSuma(op1: 2.1, op2: 5)
operacionSuma(op1: 5, op2: 5)
operacionResta(op1: 2.1, op2: 5)
operacionResta(op1: 5, op2: 5)
operacionMultiplicar(op1: 2.1, op2: 5)
operacionMultiplicar(op1: 5, op2: 5)


