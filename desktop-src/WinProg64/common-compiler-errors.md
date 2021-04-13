---
title: Errores comunes del compilador
description: En esta sección se muestran los errores de compilador típicos que se producen al migrar una base de código existente. Estos ejemplos son del código HAL de nivel de sistema, aunque los conceptos se aplican directamente a código de nivel de usuario.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- errores del compilador 64 programación de Windows de bits
- migración de 64 bits programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359530"
---
# <a name="common-compiler-errors"></a>Errores comunes del compilador

En esta sección se muestran los errores de compilador típicos que se producen al migrar una base de código existente. Estos ejemplos son del código HAL de nivel de sistema, aunque los conceptos se aplican directamente a código de nivel de usuario.

## <a name="warning-c4311-example-1"></a>ADVERTENCIA C4311 ejemplo 1

' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

**PtrToUlong** es una función insertada o una macro, dependiendo de su uso. Trunca un puntero a un **ULong**. Aunque los punteros de 32 bits no se ven afectados, se trunca la mitad superior de un puntero de 64 bits.

CIA \_ PCI \_ config \_ base \_ QVA se declara como **PVOID**. La conversión de **ULong** funciona en el mundo de 32 bits, pero produce un error en el mundo de 64 bits. La solución consiste en obtener un puntero de 64 bits a un **ULong**, ya que el cambio de la definición de la Unión que pPciAddr->u. AsULONG se define en cambia demasiado código.

Se permite el uso de la macro **PtrToUlong** para convertir el **PVOID** de 64 bits en el **ULong** necesario porque tenemos conocimiento sobre el valor específico de CIA \_ PCI \_ config \_ base \_ QVA. En este caso, este puntero nunca tendrá datos en los 32 bits superiores.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>ADVERTENCIA C4311 ejemplo 2

' tipo de conversión ': truncamiento de puntero de ' struct \_ error \_ Frame \* \_ \_ ptr64 ' a ' unsigned Long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

El problema es que el último parámetro de esta función es un puntero a una estructura de datos. Dado que PUncorrectableError es un puntero, cambia el tamaño con el modelo de programación. El prototipo de **KeBugCheckEx** se cambió para que el último parámetro sea un **ULong \_ ptr**. Como resultado, es necesario convertir el puntero de función a **ULong \_ ptr**.

Podría preguntar por qué no se usó **PVOID** como el último parámetro. Dependiendo del contexto de la llamada, el último parámetro puede ser un valor distinto de un puntero o quizás un código de error.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>ADVERTENCIA C4244 ejemplo 1

' = ': conversión de ' struct \_ Configuration \_ Component \* \_ \_ ptr64 ' a ' struct \_ Configuration \_ Component \* ', posible pérdida de datos

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

La función declara el componente variable como un componente PCONFIGURATION \_ . Más adelante, la variable se utiliza en la asignación siguiente que parece correcta:

`Component = &CurrentEntry->ComponentEntry;`

Sin embargo, el componente Type PCONFIGURATION \_ se define como:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

La definición de tipo para el \_ componente PCONFIGURATION proporciona un puntero de 32 bits en los modelos de 32 bits y de 64 bits porque está declarado como el **puntero \_ 32**. El diseñador original de esta estructura sabía que se iba a utilizar en un contexto de 32 bits en el BIOS y lo definió expresamente para ese uso. Este código funciona correctamente en Windows de 32 bits porque los punteros son de 32 bits. En Windows de 64 bits, no funciona porque el código está en el contexto de 64 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Para solucionar este problema, use \_ el componente de configuración \* en lugar del componente PCONFIGURATION de 32 bits \_ . Es importante comprender claramente el propósito del código. Si este código está diseñado para tocar el espacio del sistema o BIOS de 32 bits, esta corrección no funcionará.

El **puntero \_ 32** se define en Ntdef. h y en Winnt. h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>ADVERTENCIA C4242 ejemplo 2

' = ': conversión de ' \_ \_ Int64 ' a ' unsigned Long ', posible pérdida de datos

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Esta advertencia se genera porque el cálculo está usando valores de 64 bits, en este caso los punteros, y coloca el resultado en un **ULong** de 32 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Tipo convierta el resultado del cálculo en **ULong** como se muestra aquí:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Conversión el resultado permite que el compilador sepa que está seguro sobre el resultado. Dicho esto, asegúrese de que comprende el cálculo y, en realidad, asegúrese de que quepa en un **ULong** de 32 bits.

Si el resultado no cabe en un **ULong** de 32 bits, cambie el tipo base de la variable que contendrá el resultado.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>ADVERTENCIA C4311: ejemplo 1

' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Esta función completa trata las direcciones como enteros, lo que requiere la necesidad de escribir esos enteros de una manera portátil. Todas las variables locales, los valores intermedios de los cálculos y los valores devueltos deben ser tipos portátiles.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

**PULONG \_ PTR** es un puntero que es en sí mismo 32 bits para Windows de 32 bits y 64 bits para Windows de 64 bits. Apunta a un entero sin signo, **ULong \_ ptr**, que es 32 bits para Windows de 32 bits y los bits de 64 para Windows de 64 bits.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>ADVERTENCIA C4311: ejemplo 2

' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Aunque todos los valores de QVA (cuasi virtual Address) son en realidad valores de 32 bits en esta fase y se ajustan en un **ULong**, es más coherente tratar todas las direcciones como valores de **ULong \_ ptr** siempre que sea posible.

El puntero PciIoSpaceBase contiene el QVA que se crea en la macro HAL \_ Make \_ QVA. Esta macro devuelve un valor de 64 bits con los bits superiores de 32 establecidos en cero, por lo que la expresión matemática funcionará. Podríamos dejar simplemente el código para truncar el puntero en un **ULong**, pero esta práctica no se recomienda para mejorar la portabilidad y el mantenimiento del código. Por ejemplo, el contenido de un QVA podría cambiar en el futuro para usar algunos de los bits superiores en este nivel, interrumpiendo el código.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Ser seguro y usar **ULong \_ ptr** para todas las matemáticas de dirección y puntero.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>ADVERTENCIA C4311 ejemplo 3

' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

El compilador advierte sobre la dirección de los operadores (&) y de desplazamiento a la izquierda (<<) si se aplican a los tipos de puntero. En el código anterior, Qva es un valor de **PVOID** . Necesitamos convertirlo en un tipo entero para realizar las operaciones matemáticas. Dado que el código debe ser portable, use **ULong \_ ptr** en lugar de **ULong**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>ADVERTENCIA C4311 ejemplo 4

' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

TranslatedAddress es una Unión que tiene un aspecto similar al siguiente:

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Conociendo lo que el resto del código podría colocar en Highpart, podemos seleccionar cualquiera de las soluciones que se muestran aquí.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

La macro **PtrToUlong** trunca el puntero devuelto por **HalCreateQva** a 32 bits. Sabemos que el QVA devuelto por **HalCreateQva** tiene los bits superiores 32 establecidos en cero y la siguiente línea de código establece TranslatedAddress->Highpart en cero.

Con precaución, podríamos utilizar lo siguiente:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Esto funciona en este ejemplo: la macro **HalCreateQva** devuelve 64 bits, con los bits superiores 32 establecidos en cero. Tenga cuidado de no dejar los 32 bits superiores sin definir en un entorno de 32 bits, que esta segunda solución puede hacer realmente.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>ADVERTENCIA C4311 ejemplo 5

' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

WindowRegisters->WindowBase es un puntero y ahora es 64 bits. En el código, se indica al desplazamiento a la derecha este valor 20 bits. El compilador no nos permitirá usar el operador de desplazamiento a la derecha (>>) en un puntero; por lo tanto, es necesario convertirlo en algún tipo de entero.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

La conversión a **ULong \_ ptr** es exactamente lo que necesitamos. El siguiente problema es WBase. WBase es **ULong** y es 32 bits. En este caso, sabemos que el puntero de 64 bits WindowRegisters->WindowBase es válido en los 32 bits inferiores incluso después de desplazarse. Esto hace que el uso de la macro **PtrToUlong** sea aceptable, ya que truncará el puntero de 64 bits en un **ULong** de 32 bits. La conversión de **PVOID** es necesaria porque **PtrToUlong** espera un argumento de puntero. Al examinar el código del ensamblador resultante, toda esta conversión de código de C se convierte en una carga cuádruple, desplazarse a la derecha y almacenar larga.

</dd> </dl>

 

 




