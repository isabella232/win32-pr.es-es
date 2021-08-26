---
title: Errores comunes del compilador
description: En esta sección se muestran los errores típicos del compilador que se producen al migrar una base de código existente. Estos ejemplos proceden del código DE ACUERDO de nivel de sistema, aunque los conceptos son directamente aplicables al código de nivel de usuario.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- errores del compilador de 64 bits Windows programación
- programación de migración de 64 Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d12e7c5566b5cb2b934eefb71b1b51858f278d3e408d3080cb1810f185dcfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071645"
---
# <a name="common-compiler-errors"></a>Errores comunes del compilador

En esta sección se muestran los errores típicos del compilador que se producen al migrar una base de código existente. Estos ejemplos proceden del código DE ACUERDO de nivel de sistema, aunque los conceptos son directamente aplicables al código de nivel de usuario.

## <a name="warning-c4311-example-1"></a>Advertencia C4311 Ejemplo 1

'type cast': truncamiento del puntero de 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

**PtrToUlong es** una función insertda o una macro, en función de su uso. Trunca un puntero a un **ULONG.** Aunque los punteros de 32 bits no se ven afectados, se trunca la mitad superior de un puntero de 64 bits.

PCI \_ \_ CONFIG BASE \_ \_ QVA se declara como **PVOID**. La **conversión ULONG** funciona en el mundo de 32 bits, pero produce un error en el mundo de 64 bits. La solución es obtener un puntero de 64 bits a **un ULONG**, porque cambiar la definición de la unión que pPciAddr->u.AsULONG se define en cambia demasiado código.

Se permite el uso de la macro **PtrToUlong** para convertir el **PVOID** de 64 bits en el **ULONG** necesario porque tenemos conocimientos sobre el valor específico de QVA base PCI CONFIG de LA \_ \_ \_ \_ PCI. En este caso, este puntero nunca tendrá datos en los 32 bits superiores.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Advertencia C4311 Ejemplo 2

'type cast': truncamiento de puntero de 'struct \_ ERROR \_ FRAME \* \_ \_ ptr64' a 'unsigned long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

El problema es que el último parámetro de esta función es un puntero a una estructura de datos. Dado que PUncorrectableError es un puntero, cambia de tamaño con el modelo de programación. Se ha cambiado **el prototipo de KeCheckCheckEx** para que el último parámetro sea **ULONG \_ PTR.** Como resultado, es necesario convertir el puntero de función a **ULONG \_ PTR**.

Puede preguntar por qué **PVOID** no se usó como último parámetro. Dependiendo del contexto de la llamada, el último parámetro puede ser distinto de un puntero o quizás un código de error.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Advertencia C4244 Ejemplo 1

'=': conversión de 'struct \_ CONFIGURATION \_ COMPONENT \* \_ \_ ptr64' a 'struct CONFIGURATION \_ \_ \* COMPONENT', posible pérdida de datos

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

La función declara la variable Component como PCONFIGURATION \_ COMPONENT. Más adelante, la variable se usa en la siguiente asignación que parece correcta:

`Component = &CurrentEntry->ComponentEntry;`

Sin embargo, el tipo PCONFIGURATION \_ COMPONENT se define como:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

La definición de tipo para PCONFIGURATION COMPONENT proporciona un puntero de 32 bits en los modelos de 32 bits y 64 bits porque se \_ declara **POINTER \_ 32**. El diseñador original de esta estructura sabía que se usaría en un contexto de 32 bits en el BIOS y lo definió expresamente para ese uso. Este código funciona bien en archivos de 32 Windows porque los punteros son de 32 bits. En las Windows de 64 bits, no funciona porque el código está en contexto de 64 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Para solucionar este problema, use CONFIGURATION \_ COMPONENT en lugar de \* PCONFIGURATION COMPONENT de 32 \_ bits. Es importante comprender claramente el propósito del código. Si este código está pensado para tocar el bios de 32 bits o el espacio del sistema, esta corrección no funcionará.

**POINTER \_ 32** se define en Ntdef.h y Winnt.h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Advertencia C4242 Ejemplo 2

'=': conversión de \_ \_ 'int64' a 'unsigned long', posible pérdida de datos

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Esta advertencia se genera porque el cálculo usa valores de 64 bits, en este caso punteros, y coloca el resultado en un ULONG de 32 **bits.**

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Escriba cast the result of the calculation to a ULONG (Convertir el resultado del cálculo en **ULONG),** como se muestra aquí:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

La difusión de tipos del resultado permite al compilador saber que está seguro sobre el resultado. Dicho esto, asegúrese de que comprende el cálculo y realmente está seguro de que encajará en un ULONG de 32 **bits.**

Si el resultado puede no caber en un **ULONG** de 32 bits, cambie el tipo base de la variable que contendrán el resultado.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Advertencia C4311: ejemplo 1

'type cast': truncamiento del puntero de 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Esta función completa trata las direcciones como enteros, lo que requiere la necesidad de escribir esos enteros de una manera portátil. Todas las variables locales, los valores intermedios en los cálculos y los valores devueltos deben ser tipos portátiles.

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

**PULONG \_ PTR** es un puntero de 32 bits para 32 bits Windows y 64 bits para 64 bits Windows. Apunta a un entero sin signo, **ULONG \_ PTR**, que es de 32 bits para el Windows de 32 bits y de 64 bits para el Windows de 64 bits.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Advertencia C4311: ejemplo 2

'type cast': truncamiento del puntero de 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Aunque todos los valores de QVA (Dirección virtual cuasi) son realmente valores de 32 bits en esta fase y se ajustarán a **un ULONG,** es más coherente tratar todas las direcciones como valores **\_ ULONG PTR** siempre que sea posible.

El puntero PciIoSpaceBase contiene la QVA que se crea en la macro HAN \_ MAKE \_ QVA. Esta macro devuelve un valor de 64 bits con los 32 bits superiores establecidos en cero para que las matemáticas funcionen. Simplemente podríamos dejar el código para truncar el puntero en un **ULONG,** pero se desaconseja esta práctica para mejorar la portabilidad y el mantenimiento del código. Por ejemplo, el contenido de una QVA podría cambiar en el futuro para usar algunos de los bits superiores en este nivel, lo que podría dividir el código.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

Sea seguro y use **ULONG \_ PTR para** todas las matemáticas de dirección y puntero.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Advertencia C4311 Ejemplo 3

'type cast': truncamiento del puntero de 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

El compilador advierte sobre la dirección de (&) y los operadores de desplazamiento izquierdo (<<) si se aplican a tipos de puntero. En el código anterior, Qva es un **valor PVOID.** Es necesario convertirla en un tipo entero para realizar las operaciones matemáticas. Dado que el código debe ser portátil, use **ULONG \_ PTR en** lugar de **ULONG**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Advertencia C4311 Ejemplo 4

'type cast': truncamiento del puntero de 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

TranslatedAddress es una unión similar a la siguiente:

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

Sabiendo lo que el resto del código podría colocar en Highpart, podemos seleccionar cualquiera de las soluciones que se muestran aquí.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

La **macro PtrToUlong** trunca el puntero devuelto por **VerbCreateQva** a 32 bits. Sabemos que la QVA devuelta **porPericreateQva** tiene los 32 bits superiores establecidos en cero y la siguiente línea de código establece TranslatedAddress->Highpart en cero.

Con precaución, podríamos usar lo siguiente:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Esto funciona en este ejemplo: la macro **HacreateQva** devuelve 64 bits, con los 32 bits superiores establecidos en cero. Tenga cuidado de no dejar los 32 bits superiores sin definir en un entorno de 32 bits, lo que esta segunda solución puede hacer realmente.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Advertencia C4311 Ejemplo 5

'type cast': truncamiento del puntero de 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

WindowRegisters->WindowBase es un puntero y ahora tiene 64 bits. El código indica para desplazar a la derecha este valor de 20 bits. El compilador no nos permitirá usar el operador de desplazamiento a la derecha (>>) en un puntero; por lo tanto, es necesario convertirla en algún tipo de entero.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

La conversión a **ULONG \_ PTR** es justo lo que necesitamos. El siguiente problema es Wbase. Wbase es un **ULONG** y tiene 32 bits. En este caso, sabemos que el puntero de 64 bits WindowRegisters->WindowBase es válido en los 32 bits inferiores incluso después de desplazarse. Esto hace que el uso de la macro **PtrToUlong** sea aceptable, ya que truncará el puntero de 64 bits en un ULONG de 32 **bits.** La **conversión PVOID** es necesaria porque **PtrToUlong** espera un argumento de puntero. Cuando se observa el código ensamblador resultante, toda esta conversión de código de C se convierte en un cuadrándigo de carga, desplazamiento a la derecha y almacenamiento largo.

</dd> </dl>

 

 




