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
# <a name="common-compiler-errors"></a><span data-ttu-id="fb11d-106">Errores comunes del compilador</span><span class="sxs-lookup"><span data-stu-id="fb11d-106">Common Compiler Errors</span></span>

<span data-ttu-id="fb11d-107">En esta sección se muestran los errores de compilador típicos que se producen al migrar una base de código existente.</span><span class="sxs-lookup"><span data-stu-id="fb11d-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="fb11d-108">Estos ejemplos son del código HAL de nivel de sistema, aunque los conceptos se aplican directamente a código de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="fb11d-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="fb11d-109">ADVERTENCIA C4311 ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb11d-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="fb11d-110">' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long</span><span class="sxs-lookup"><span data-stu-id="fb11d-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="fb11d-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-113">**PtrToUlong** es una función insertada o una macro, dependiendo de su uso.</span><span class="sxs-lookup"><span data-stu-id="fb11d-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="fb11d-114">Trunca un puntero a un **ULong**.</span><span class="sxs-lookup"><span data-stu-id="fb11d-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="fb11d-115">Aunque los punteros de 32 bits no se ven afectados, se trunca la mitad superior de un puntero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="fb11d-116">CIA \_ PCI \_ config \_ base \_ QVA se declara como **PVOID**.</span><span class="sxs-lookup"><span data-stu-id="fb11d-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="fb11d-117">La conversión de **ULong** funciona en el mundo de 32 bits, pero produce un error en el mundo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="fb11d-118">La solución consiste en obtener un puntero de 64 bits a un **ULong**, ya que el cambio de la definición de la Unión que pPciAddr->u. AsULONG se define en cambia demasiado código.</span><span class="sxs-lookup"><span data-stu-id="fb11d-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="fb11d-119">Se permite el uso de la macro **PtrToUlong** para convertir el **PVOID** de 64 bits en el **ULong** necesario porque tenemos conocimiento sobre el valor específico de CIA \_ PCI \_ config \_ base \_ QVA.</span><span class="sxs-lookup"><span data-stu-id="fb11d-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="fb11d-120">En este caso, este puntero nunca tendrá datos en los 32 bits superiores.</span><span class="sxs-lookup"><span data-stu-id="fb11d-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="fb11d-122">ADVERTENCIA C4311 ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb11d-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="fb11d-123">' tipo de conversión ': truncamiento de puntero de ' struct \_ error \_ Frame \* \_ \_ ptr64 ' a ' unsigned Long</span><span class="sxs-lookup"><span data-stu-id="fb11d-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="fb11d-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-126">El problema es que el último parámetro de esta función es un puntero a una estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="fb11d-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="fb11d-127">Dado que PUncorrectableError es un puntero, cambia el tamaño con el modelo de programación.</span><span class="sxs-lookup"><span data-stu-id="fb11d-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="fb11d-128">El prototipo de **KeBugCheckEx** se cambió para que el último parámetro sea un **ULong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="fb11d-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="fb11d-129">Como resultado, es necesario convertir el puntero de función a **ULong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="fb11d-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="fb11d-130">Podría preguntar por qué no se usó **PVOID** como el último parámetro.</span><span class="sxs-lookup"><span data-stu-id="fb11d-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="fb11d-131">Dependiendo del contexto de la llamada, el último parámetro puede ser un valor distinto de un puntero o quizás un código de error.</span><span class="sxs-lookup"><span data-stu-id="fb11d-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="fb11d-133">ADVERTENCIA C4244 ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb11d-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="fb11d-134">' = ': conversión de ' struct \_ Configuration \_ Component \* \_ \_ ptr64 ' a ' struct \_ Configuration \_ Component \* ', posible pérdida de datos</span><span class="sxs-lookup"><span data-stu-id="fb11d-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="fb11d-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-137">La función declara el componente variable como un componente PCONFIGURATION \_ .</span><span class="sxs-lookup"><span data-stu-id="fb11d-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="fb11d-138">Más adelante, la variable se utiliza en la asignación siguiente que parece correcta:</span><span class="sxs-lookup"><span data-stu-id="fb11d-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="fb11d-139">Sin embargo, el componente Type PCONFIGURATION \_ se define como:</span><span class="sxs-lookup"><span data-stu-id="fb11d-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="fb11d-140">La definición de tipo para el \_ componente PCONFIGURATION proporciona un puntero de 32 bits en los modelos de 32 bits y de 64 bits porque está declarado como el **puntero \_ 32**.</span><span class="sxs-lookup"><span data-stu-id="fb11d-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="fb11d-141">El diseñador original de esta estructura sabía que se iba a utilizar en un contexto de 32 bits en el BIOS y lo definió expresamente para ese uso.</span><span class="sxs-lookup"><span data-stu-id="fb11d-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="fb11d-142">Este código funciona correctamente en Windows de 32 bits porque los punteros son de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="fb11d-143">En Windows de 64 bits, no funciona porque el código está en el contexto de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-145">Para solucionar este problema, use \_ el componente de configuración \* en lugar del componente PCONFIGURATION de 32 bits \_ .</span><span class="sxs-lookup"><span data-stu-id="fb11d-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="fb11d-146">Es importante comprender claramente el propósito del código.</span><span class="sxs-lookup"><span data-stu-id="fb11d-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="fb11d-147">Si este código está diseñado para tocar el espacio del sistema o BIOS de 32 bits, esta corrección no funcionará.</span><span class="sxs-lookup"><span data-stu-id="fb11d-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="fb11d-148">El **puntero \_ 32** se define en Ntdef. h y en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="fb11d-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="fb11d-149">ADVERTENCIA C4242 ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb11d-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="fb11d-150">' = ': conversión de ' \_ \_ Int64 ' a ' unsigned Long ', posible pérdida de datos</span><span class="sxs-lookup"><span data-stu-id="fb11d-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="fb11d-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-153">Esta advertencia se genera porque el cálculo está usando valores de 64 bits, en este caso los punteros, y coloca el resultado en un **ULong** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-155">Tipo convierta el resultado del cálculo en **ULong** como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="fb11d-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="fb11d-156">Conversión el resultado permite que el compilador sepa que está seguro sobre el resultado.</span><span class="sxs-lookup"><span data-stu-id="fb11d-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="fb11d-157">Dicho esto, asegúrese de que comprende el cálculo y, en realidad, asegúrese de que quepa en un **ULong** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="fb11d-158">Si el resultado no cabe en un **ULong** de 32 bits, cambie el tipo base de la variable que contendrá el resultado.</span><span class="sxs-lookup"><span data-stu-id="fb11d-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="fb11d-159">ADVERTENCIA C4311: ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb11d-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="fb11d-160">' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '</span><span class="sxs-lookup"><span data-stu-id="fb11d-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="fb11d-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-163">Esta función completa trata las direcciones como enteros, lo que requiere la necesidad de escribir esos enteros de una manera portátil.</span><span class="sxs-lookup"><span data-stu-id="fb11d-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="fb11d-164">Todas las variables locales, los valores intermedios de los cálculos y los valores devueltos deben ser tipos portátiles.</span><span class="sxs-lookup"><span data-stu-id="fb11d-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
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

<span data-ttu-id="fb11d-166">**PULONG \_ PTR** es un puntero que es en sí mismo 32 bits para Windows de 32 bits y 64 bits para Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="fb11d-167">Apunta a un entero sin signo, **ULong \_ ptr**, que es 32 bits para Windows de 32 bits y los bits de 64 para Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="fb11d-168">ADVERTENCIA C4311: ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb11d-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="fb11d-169">' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '</span><span class="sxs-lookup"><span data-stu-id="fb11d-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="fb11d-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-172">Aunque todos los valores de QVA (cuasi virtual Address) son en realidad valores de 32 bits en esta fase y se ajustan en un **ULong**, es más coherente tratar todas las direcciones como valores de **ULong \_ ptr** siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="fb11d-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="fb11d-173">El puntero PciIoSpaceBase contiene el QVA que se crea en la macro HAL \_ Make \_ QVA.</span><span class="sxs-lookup"><span data-stu-id="fb11d-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="fb11d-174">Esta macro devuelve un valor de 64 bits con los bits superiores de 32 establecidos en cero, por lo que la expresión matemática funcionará.</span><span class="sxs-lookup"><span data-stu-id="fb11d-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="fb11d-175">Podríamos dejar simplemente el código para truncar el puntero en un **ULong**, pero esta práctica no se recomienda para mejorar la portabilidad y el mantenimiento del código.</span><span class="sxs-lookup"><span data-stu-id="fb11d-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="fb11d-176">Por ejemplo, el contenido de un QVA podría cambiar en el futuro para usar algunos de los bits superiores en este nivel, interrumpiendo el código.</span><span class="sxs-lookup"><span data-stu-id="fb11d-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-178">Ser seguro y usar **ULong \_ ptr** para todas las matemáticas de dirección y puntero.</span><span class="sxs-lookup"><span data-stu-id="fb11d-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="fb11d-179">ADVERTENCIA C4311 ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="fb11d-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="fb11d-180">' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '</span><span class="sxs-lookup"><span data-stu-id="fb11d-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="fb11d-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-183">El compilador advierte sobre la dirección de los operadores (&) y de desplazamiento a la izquierda (<<) si se aplican a los tipos de puntero.</span><span class="sxs-lookup"><span data-stu-id="fb11d-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="fb11d-184">En el código anterior, Qva es un valor de **PVOID** .</span><span class="sxs-lookup"><span data-stu-id="fb11d-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="fb11d-185">Necesitamos convertirlo en un tipo entero para realizar las operaciones matemáticas.</span><span class="sxs-lookup"><span data-stu-id="fb11d-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="fb11d-186">Dado que el código debe ser portable, use **ULong \_ ptr** en lugar de **ULong**.</span><span class="sxs-lookup"><span data-stu-id="fb11d-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="fb11d-188">ADVERTENCIA C4311 ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="fb11d-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="fb11d-189">' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '</span><span class="sxs-lookup"><span data-stu-id="fb11d-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="fb11d-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-192">TranslatedAddress es una Unión que tiene un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb11d-192">TranslatedAddress is a union that looks something like the following:</span></span>

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

<span data-ttu-id="fb11d-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-194">Conociendo lo que el resto del código podría colocar en Highpart, podemos seleccionar cualquiera de las soluciones que se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="fb11d-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="fb11d-195">La macro **PtrToUlong** trunca el puntero devuelto por **HalCreateQva** a 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="fb11d-196">Sabemos que el QVA devuelto por **HalCreateQva** tiene los bits superiores 32 establecidos en cero y la siguiente línea de código establece TranslatedAddress->Highpart en cero.</span><span class="sxs-lookup"><span data-stu-id="fb11d-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="fb11d-197">Con precaución, podríamos utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb11d-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="fb11d-198">Esto funciona en este ejemplo: la macro **HalCreateQva** devuelve 64 bits, con los bits superiores 32 establecidos en cero.</span><span class="sxs-lookup"><span data-stu-id="fb11d-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="fb11d-199">Tenga cuidado de no dejar los 32 bits superiores sin definir en un entorno de 32 bits, que esta segunda solución puede hacer realmente.</span><span class="sxs-lookup"><span data-stu-id="fb11d-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="fb11d-200">ADVERTENCIA C4311 ejemplo 5</span><span class="sxs-lookup"><span data-stu-id="fb11d-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="fb11d-201">' tipo de conversión ': truncamiento de puntero de ' void \* \_ \_ ptr64 ' a ' unsigned Long '</span><span class="sxs-lookup"><span data-stu-id="fb11d-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="fb11d-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="fb11d-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="fb11d-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="fb11d-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fb11d-204">WindowRegisters->WindowBase es un puntero y ahora es 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="fb11d-205">En el código, se indica al desplazamiento a la derecha este valor 20 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="fb11d-206">El compilador no nos permitirá usar el operador de desplazamiento a la derecha (>>) en un puntero; por lo tanto, es necesario convertirlo en algún tipo de entero.</span><span class="sxs-lookup"><span data-stu-id="fb11d-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="fb11d-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solución</span><span class="sxs-lookup"><span data-stu-id="fb11d-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="fb11d-208">La conversión a **ULong \_ ptr** es exactamente lo que necesitamos.</span><span class="sxs-lookup"><span data-stu-id="fb11d-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="fb11d-209">El siguiente problema es WBase.</span><span class="sxs-lookup"><span data-stu-id="fb11d-209">The next problem is Wbase.</span></span> <span data-ttu-id="fb11d-210">WBase es **ULong** y es 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="fb11d-211">En este caso, sabemos que el puntero de 64 bits WindowRegisters->WindowBase es válido en los 32 bits inferiores incluso después de desplazarse.</span><span class="sxs-lookup"><span data-stu-id="fb11d-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="fb11d-212">Esto hace que el uso de la macro **PtrToUlong** sea aceptable, ya que truncará el puntero de 64 bits en un **ULong** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb11d-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="fb11d-213">La conversión de **PVOID** es necesaria porque **PtrToUlong** espera un argumento de puntero.</span><span class="sxs-lookup"><span data-stu-id="fb11d-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="fb11d-214">Al examinar el código del ensamblador resultante, toda esta conversión de código de C se convierte en una carga cuádruple, desplazarse a la derecha y almacenar larga.</span><span class="sxs-lookup"><span data-stu-id="fb11d-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 




