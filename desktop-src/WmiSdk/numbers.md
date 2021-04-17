---
description: En MOF, los números son dígitos que describen valores numéricos. MOF proporciona una variedad de tipos de datos que se traducen en la automatización y también permite que dichos números estén en formatos diferentes. En la tabla siguiente se enumeran los valores numéricos que MOF admite.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Números (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705438"
---
# <a name="numbers-wmi"></a><span data-ttu-id="a514d-105">Números (WMI)</span><span class="sxs-lookup"><span data-stu-id="a514d-105">Numbers (WMI)</span></span>

<span data-ttu-id="a514d-106">En MOF, los números son dígitos que describen valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="a514d-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="a514d-107">MOF proporciona una variedad de tipos de datos que se traducen en la automatización y también permite que dichos números estén en formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="a514d-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="a514d-108">En la tabla siguiente se enumeran los valores numéricos que MOF admite.</span><span class="sxs-lookup"><span data-stu-id="a514d-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="a514d-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a514d-109">Data type</span></span>  | <span data-ttu-id="a514d-110">Tipo de automatización</span><span class="sxs-lookup"><span data-stu-id="a514d-110">Automation type</span></span> | <span data-ttu-id="a514d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a514d-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a514d-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="a514d-112">**sint8**</span></span>  | <span data-ttu-id="a514d-113">**I2 de VT \_**</span><span class="sxs-lookup"><span data-stu-id="a514d-113">**VT\_I2**</span></span>      | <span data-ttu-id="a514d-114">Entero de 8 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="a514d-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="a514d-115">**sint16**</span></span> | <span data-ttu-id="a514d-116">**I2 de VT \_**</span><span class="sxs-lookup"><span data-stu-id="a514d-116">**VT\_I2**</span></span>      | <span data-ttu-id="a514d-117">Entero de 16 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="a514d-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="a514d-118">**sint32**</span></span> | <span data-ttu-id="a514d-119">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a514d-119">VT\_I4</span></span>          | <span data-ttu-id="a514d-120">Entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="a514d-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="a514d-121">**sint64**</span></span> | <span data-ttu-id="a514d-122">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a514d-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="a514d-123">Entero de 64 bits con signo en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="a514d-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="a514d-124">Este tipo sigue el formato hexadecimal o decimal según las reglas de C de American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a514d-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="a514d-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="a514d-125">**real32**</span></span> | <span data-ttu-id="a514d-126">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="a514d-126">**VT\_R4**</span></span>      | <span data-ttu-id="a514d-127">valor de punto flotante de 4 bytes que sigue el estándar Institute of Electrical and Electronics Engineers, Inc. (IEEE).</span><span class="sxs-lookup"><span data-stu-id="a514d-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="a514d-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="a514d-128">**real64**</span></span> | <span data-ttu-id="a514d-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="a514d-129">**VT\_R8**</span></span>      | <span data-ttu-id="a514d-130">valor de punto flotante de 8 bytes que sigue al estándar IEEE.</span><span class="sxs-lookup"><span data-stu-id="a514d-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="a514d-131">**Uint8**</span><span class="sxs-lookup"><span data-stu-id="a514d-131">**uint8**</span></span>  | <span data-ttu-id="a514d-132">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="a514d-132">**VT\_UI1**</span></span>     | <span data-ttu-id="a514d-133">Entero de 8 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a514d-134">**uint16**</span><span class="sxs-lookup"><span data-stu-id="a514d-134">**uint16**</span></span> | <span data-ttu-id="a514d-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="a514d-135">**VT\_I4**</span></span>      | <span data-ttu-id="a514d-136">Entero de 16 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a514d-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="a514d-137">**uint32**</span></span> | <span data-ttu-id="a514d-138">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="a514d-138">**VT\_I4**</span></span>      | <span data-ttu-id="a514d-139">Entero de bit 32 sin signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a514d-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="a514d-140">**uint64**</span></span> | <span data-ttu-id="a514d-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a514d-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="a514d-142">Entero de 64 bits sin signo en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="a514d-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="a514d-143">Este tipo sigue el formato hexadecimal o decimal de acuerdo con las reglas de ANSI C.</span><span class="sxs-lookup"><span data-stu-id="a514d-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="a514d-144">Aunque es flexible, el código MOF encuentra algunos cambios al tratar con la automatización:</span><span class="sxs-lookup"><span data-stu-id="a514d-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="a514d-145">Debe codificar enteros de 64 bits como cadenas.</span><span class="sxs-lookup"><span data-stu-id="a514d-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="a514d-146">Automation no admite un tipo entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a514d-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="a514d-147">Los tipos de automatización no siempre se corresponden en tamaño de bits a los tipos de datos MOF.</span><span class="sxs-lookup"><span data-stu-id="a514d-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="a514d-148">Por ejemplo, Automation utiliza VT \_ I4 para devolver un valor de 16 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="a514d-149">Esta discrepancia existe debido a problemas de extensión de signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="a514d-150">Si Automation usaba VT \_ I2 en lugar de VT \_ I4, 65.536 sería el valor 1, lo que provocaría problemas de tipo y de intervalo.</span><span class="sxs-lookup"><span data-stu-id="a514d-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="a514d-151">Del mismo modo, Automation representa el tipo **UInt32** como VT \_ I4 porque no existe un tipo entero más grande que contenga **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="a514d-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="a514d-152">No es necesario cambiar ninguna representación de los tipos de números de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="a514d-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="a514d-153">Automation admite VT \_ UI1, un tipo de 8 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="a514d-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="a514d-154">MOF admite constantes largas.</span><span class="sxs-lookup"><span data-stu-id="a514d-154">MOF supports long constants.</span></span> <span data-ttu-id="a514d-155">Declare una constante larga mediante una serie simple de dígitos con un signo negativo opcional.</span><span class="sxs-lookup"><span data-stu-id="a514d-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="a514d-156">Una constante larga no puede superar el tamaño de la variable que se declara para contenerla.</span><span class="sxs-lookup"><span data-stu-id="a514d-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="a514d-157">Algunos ejemplos de constantes largas son 1000 y 12310.</span><span class="sxs-lookup"><span data-stu-id="a514d-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="a514d-158">MOF también admite formatos numéricos alternativos.</span><span class="sxs-lookup"><span data-stu-id="a514d-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="a514d-159">En la tabla siguiente se enumeran los caracteres especiales que se deben usar para describir las constantes hexadecimales, binarias y octales.</span><span class="sxs-lookup"><span data-stu-id="a514d-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="a514d-160">Constante</span><span class="sxs-lookup"><span data-stu-id="a514d-160">Constant</span></span>               | <span data-ttu-id="a514d-161">Carácter especial</span><span class="sxs-lookup"><span data-stu-id="a514d-161">Special character</span></span>     | <span data-ttu-id="a514d-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a514d-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="a514d-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="a514d-163">Decimal</span></span><br/>     | <span data-ttu-id="a514d-164">None</span><span class="sxs-lookup"><span data-stu-id="a514d-164">None</span></span><br/>       | <span data-ttu-id="a514d-165">Val = 65</span><span class="sxs-lookup"><span data-stu-id="a514d-165">val = 65</span></span><br/>       |
| <span data-ttu-id="a514d-166">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="a514d-166">Hexadecimal</span></span><br/> | <span data-ttu-id="a514d-167">Prefijo 0x</span><span class="sxs-lookup"><span data-stu-id="a514d-167">0x prefix</span></span><br/>  | <span data-ttu-id="a514d-168">Val = 0x41</span><span class="sxs-lookup"><span data-stu-id="a514d-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="a514d-169">Octal</span><span class="sxs-lookup"><span data-stu-id="a514d-169">Octal</span></span><br/>       | <span data-ttu-id="a514d-170">Primer 0</span><span class="sxs-lookup"><span data-stu-id="a514d-170">Leading 0</span></span><br/>  | <span data-ttu-id="a514d-171">Val = 0101</span><span class="sxs-lookup"><span data-stu-id="a514d-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="a514d-172">Binary</span><span class="sxs-lookup"><span data-stu-id="a514d-172">Binary</span></span><br/>      | <span data-ttu-id="a514d-173">B final</span><span class="sxs-lookup"><span data-stu-id="a514d-173">Trailing B</span></span><br/> | <span data-ttu-id="a514d-174">Val = 1000001B</span><span class="sxs-lookup"><span data-stu-id="a514d-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="a514d-175">Puede usar una constante de punto flotante para representar la notación científica y las fracciones, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="a514d-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="a514d-176">WMI considera las constantes de punto flotante como tipos de **VT \_ R8** para la automatización.</span><span class="sxs-lookup"><span data-stu-id="a514d-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="a514d-177">En el ejemplo siguiente se describen las declaraciones de clase e instancia que muestran cómo usar cada uno de los tipos de datos numéricos para establecer propiedades:</span><span class="sxs-lookup"><span data-stu-id="a514d-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




