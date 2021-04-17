---
title: Trasladar a Visual Basic de C++
description: Trasladar a Visual Basic de C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656287"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="acee5-103">Trasladar a Visual Basic de C++</span><span class="sxs-lookup"><span data-stu-id="acee5-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="acee5-104">Mediante el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada.</span><span class="sxs-lookup"><span data-stu-id="acee5-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="acee5-105">Los punteros de memoria proporcionan este acceso directo.</span><span class="sxs-lookup"><span data-stu-id="acee5-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="acee5-106">En Visual Basic, los punteros se controlan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="acee5-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="acee5-107">Por ejemplo, un parámetro declarado como un puntero a un **int** en C++ es equivalente a un parámetro declarado en Visual Basic como un  **entero** de ByRef.</span><span class="sxs-lookup"><span data-stu-id="acee5-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="acee5-108">Un parámetro declarado **como String** en Visual Basic se declara como un puntero a un **BSTR** en C++.</span><span class="sxs-lookup"><span data-stu-id="acee5-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="acee5-109">Establecer un puntero de cadena en **null** en C++ es equivalente a establecer la cadena en la constante **vbNullString** en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acee5-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="acee5-110">Pasar una cadena de longitud cero ("") a una función diseñada para recibir **null** no funciona, ya que pasa un puntero a una cadena de longitud cero en lugar de un puntero cero.</span><span class="sxs-lookup"><span data-stu-id="acee5-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="acee5-111">C++ admite contenedores de datos, es decir, estructuras y uniones, que no tienen ningún equivalente en versiones anteriores de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acee5-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="acee5-112">Por esta razón, los objetos COM normalmente encapsulan información que normalmente se almacena en estructuras y uniones en clases de objeto.</span><span class="sxs-lookup"><span data-stu-id="acee5-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="acee5-113">Sin embargo, algunos objetos COM pueden contener estructuras, lo que hace que no se pueda tener acceso a partes de los métodos o la funcionalidad del objeto para Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acee5-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="acee5-114">Algunos tipos de datos de C++ no se admiten en Visual Basic, por ejemplo tipos sin signo y tipos **hWnd** .</span><span class="sxs-lookup"><span data-stu-id="acee5-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="acee5-115">Los métodos que aceptan o devuelven estos tipos de datos no están disponibles en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acee5-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="acee5-116">Visual Basic usa tipos de datos compatibles con la automatización como sus tipos de datos internos.</span><span class="sxs-lookup"><span data-stu-id="acee5-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="acee5-117">Por lo tanto, los tipos de datos de C++ que son compatibles con la automatización también son compatibles con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acee5-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="acee5-118">Es posible que los tipos de datos que no son compatibles con la automatización no se puedan convertir en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acee5-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="acee5-119">En la tabla siguiente se enumeran los tipos de datos admitidos por Visual Basic y sus equivalentes de **VARTYPE** .</span><span class="sxs-lookup"><span data-stu-id="acee5-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="acee5-120">**VARTYPE** es una enumeración que enumera los tipos de variante de automatización.</span><span class="sxs-lookup"><span data-stu-id="acee5-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="acee5-121">Tipo de datos en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="acee5-121">Visual Basic data type</span></span>  | <span data-ttu-id="acee5-122">Equivalente de VARTYPE</span><span class="sxs-lookup"><span data-stu-id="acee5-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="acee5-123">**Entero**</span><span class="sxs-lookup"><span data-stu-id="acee5-123">**Integer**</span></span><br/>  | <span data-ttu-id="acee5-124">I2 de 16 bits, con signo y VT \_</span><span class="sxs-lookup"><span data-stu-id="acee5-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="acee5-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="acee5-125">**Long**</span></span><br/>     | <span data-ttu-id="acee5-126">32 bits, con signo, VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="acee5-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="acee5-127">**Date**</span><span class="sxs-lookup"><span data-stu-id="acee5-127">**Date**</span></span><br/>     | <span data-ttu-id="acee5-128">fecha de VT \_</span><span class="sxs-lookup"><span data-stu-id="acee5-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="acee5-129">**Moneda**</span><span class="sxs-lookup"><span data-stu-id="acee5-129">**Currency**</span></span><br/> | <span data-ttu-id="acee5-130">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="acee5-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="acee5-131">**Object**</span><span class="sxs-lookup"><span data-stu-id="acee5-131">**Object**</span></span><br/>   | <span data-ttu-id="acee5-132">\*distribución de VT \_</span><span class="sxs-lookup"><span data-stu-id="acee5-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="acee5-133">**String**</span><span class="sxs-lookup"><span data-stu-id="acee5-133">**String**</span></span><br/>   | <span data-ttu-id="acee5-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="acee5-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="acee5-135">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="acee5-135">**Boolean**</span></span><br/>  | <span data-ttu-id="acee5-136">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="acee5-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="acee5-137">**Moneda**</span><span class="sxs-lookup"><span data-stu-id="acee5-137">**Currency**</span></span><br/> | <span data-ttu-id="acee5-138">VT \_ decimal</span><span class="sxs-lookup"><span data-stu-id="acee5-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="acee5-139">**Single**</span><span class="sxs-lookup"><span data-stu-id="acee5-139">**Single**</span></span><br/>   | <span data-ttu-id="acee5-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="acee5-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="acee5-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="acee5-141">**Double**</span></span><br/>   | <span data-ttu-id="acee5-142">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="acee5-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="acee5-143">**Decimal**</span><span class="sxs-lookup"><span data-stu-id="acee5-143">**Decimal**</span></span><br/>  | <span data-ttu-id="acee5-144">VT \_ decimal</span><span class="sxs-lookup"><span data-stu-id="acee5-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="acee5-145">**Byte**</span><span class="sxs-lookup"><span data-stu-id="acee5-145">**Byte**</span></span><br/>     | <span data-ttu-id="acee5-146">VT \_ decimal</span><span class="sxs-lookup"><span data-stu-id="acee5-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="acee5-147">**Variante**</span><span class="sxs-lookup"><span data-stu-id="acee5-147">**Variant**</span></span><br/>  | <span data-ttu-id="acee5-148">VT ( \_ variante)</span><span class="sxs-lookup"><span data-stu-id="acee5-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="acee5-149">Todos los parámetros de Visual Basic, a menos que se etiqueten con la palabra clave **ByVal**, se pasan por referencia (como punteros) en lugar de por valor.</span><span class="sxs-lookup"><span data-stu-id="acee5-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="acee5-150">C++ y Visual Basic difieren ligeramente en la forma en que representan las propiedades.</span><span class="sxs-lookup"><span data-stu-id="acee5-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="acee5-151">En C++, las propiedades se representan como un conjunto de funciones de descriptor de acceso, una que establece el valor de propiedad y otra que recupera el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="acee5-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="acee5-152">En Visual Basic, las propiedades se representan como un único elemento que se puede utilizar para recuperar o establecer el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="acee5-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acee5-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acee5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acee5-154">Trasladar a Visual Basic</span><span class="sxs-lookup"><span data-stu-id="acee5-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





