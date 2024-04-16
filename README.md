# Caso Automotora v02

## Descripción del Problema

Una automotora desea implementar un software capaz de mostrar todos los vehículos que tiene a la venta en sus diferentes sedes, especificando su nombre, año, precio, kilómetros recorridos, color y marca.

Además, se desea almacenar información con respecto a un cliente. De este usuario se desea saber su nombre, dirección, número telefónico, correo electrónico y rut.

Con respecto a las funcionalidades del sistema, se requiere:

- Agregar Clientes
- Agregar Vehículos
- Buscar Vehículos

Se deben realizar validaciones al momento de ingresar un correo electrónico o rut. Para el correo electrónico, se valida que haya al menos un carácter "@". Para la verificación del rut, se valida con el dígito verificador.

## Funcionalidades

1. Agregar Clientes:
   - Permite agregar un nuevo cliente con su información personal.
   - Se validan los datos ingresados, incluyendo el correo electrónico y el rut.

2. Agregar Vehículos:
   - Permite agregar un nuevo vehículo con su información detallada.
   - Se validan los datos ingresados para garantizar su integridad.

3. Buscar Vehículos:
   - Permite buscar vehículos según diferentes criterios, como marca, año, precio, etc.
   - Proporciona una lista de vehículos que coinciden con los criterios de búsqueda especificados.

## Diagrama de Clases

```
[Incluir aquí el diagrama de clases UML]
```

## Clases, Atributos y Métodos

### Clase Cliente

- **Atributos:**
  - nombre: String
  - direccion: String
  - telefono: String
  - email: String
  - rut: String

- **Métodos:**
  - agregarCliente(nombre: String, direccion: String, telefono: String, email: String, rut: String): void
  - validarEmail(email: String): boolean
  - validarRut(rut: String): boolean

### Clase Vehiculo

- **Atributos:**
  - nombre: String
  - año: int
  - precio: double
  - kilometros: double
  - color: String
  - marca: String

- **Métodos:**
  - agregarVehiculo(nombre: String, año: int, precio: double, kilometros: double, color: String, marca: String): void

### Clase AutomotoraController (Controlador)

- **Métodos:**
  - agregarCliente(nombre: String, direccion: String, telefono: String, email: String, rut: String): void
  - agregarVehiculo(nombre: String, año: int, precio: double, kilometros: double, color: String, marca: String): void
  - buscarVehiculos(criteriosBusqueda: Map<String, String>): ArrayList<Vehiculo>

### Clase AutomotoraView (Vista)

- **Métodos:**
  - mostrarMenuPrincipal(): void
  - mostrarFormularioAgregarCliente(): void
  - mostrarFormularioAgregarVehiculo(): void
  - mostrarResultadosBusquedaVehiculos(vehiculos: ArrayList<Vehiculo>): void

## Relaciones entre Clases

- La clase `Cliente` tiene una asociación con la clase `AutomotoraController` para agregar clientes.
- La clase `Vehiculo` tiene una asociación con la clase `AutomotoraController` para agregar vehículos.
- La clase `AutomotoraView` tiene una asociación con la clase `AutomotoraController` para manejar la interacción con el usuario.

Esta plantilla proporciona una estructura básica para abordar el problema planteado y se puede completar con detalles adicionales según sea necesario.
