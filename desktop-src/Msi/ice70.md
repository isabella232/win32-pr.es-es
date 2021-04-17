---
description: ICE70 comprueba que los valores enteros de las entradas del registro se especifican correctamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668069"
---
# <a name="ice70"></a><span data-ttu-id="2207e-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="2207e-103">ICE70</span></span>

<span data-ttu-id="2207e-104">ICE70 comprueba que los valores enteros de las entradas del registro se especifican correctamente.</span><span class="sxs-lookup"><span data-stu-id="2207e-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="2207e-105">\# \# No se validan los valores del formato Str, \# % sin expandir.</span><span class="sxs-lookup"><span data-stu-id="2207e-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="2207e-106">Se validan los valores de la forma \# xhex, \# xhex, \# Integer y \# \[ Property \] .</span><span class="sxs-lookup"><span data-stu-id="2207e-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="2207e-107">En la tabla siguiente se proporciona una breve introducción.</span><span class="sxs-lookup"><span data-stu-id="2207e-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="2207e-108">Value</span><span class="sxs-lookup"><span data-stu-id="2207e-108">Value</span></span>                 | <span data-ttu-id="2207e-109">Validación</span><span class="sxs-lookup"><span data-stu-id="2207e-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2207e-110">\#\#CAD</span><span class="sxs-lookup"><span data-stu-id="2207e-110">\#\#str</span></span>               | <span data-ttu-id="2207e-111">válido</span><span class="sxs-lookup"><span data-stu-id="2207e-111">valid</span></span>                                                                         |
| <span data-ttu-id="2207e-112">\#% de Str no expandido</span><span class="sxs-lookup"><span data-stu-id="2207e-112">\#%unexpanded str</span></span>     | <span data-ttu-id="2207e-113">válido</span><span class="sxs-lookup"><span data-stu-id="2207e-113">valid</span></span>                                                                         |
| <span data-ttu-id="2207e-114">\#xHex, \# xHex</span><span class="sxs-lookup"><span data-stu-id="2207e-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="2207e-115">Valide los caracteres hexadecimales válidos (0-9, a-f, A-F).</span><span class="sxs-lookup"><span data-stu-id="2207e-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="2207e-116">Aquí se permiten las propiedades.</span><span class="sxs-lookup"><span data-stu-id="2207e-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="2207e-117">\#+ int, \# -int, \# int</span><span class="sxs-lookup"><span data-stu-id="2207e-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="2207e-118">Valide los caracteres numéricos válidos (0-9).</span><span class="sxs-lookup"><span data-stu-id="2207e-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="2207e-119">Aquí se permiten las propiedades.</span><span class="sxs-lookup"><span data-stu-id="2207e-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="2207e-120">La sintaxis de un valor entero que se va a escribir en el registro es un \# entero en el que el entero es numérico.</span><span class="sxs-lookup"><span data-stu-id="2207e-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="2207e-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="2207e-121">Result</span></span>

<span data-ttu-id="2207e-122">ICE70 informa de un error si los valores enteros de las entradas del registro no se especifican correctamente.</span><span class="sxs-lookup"><span data-stu-id="2207e-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="2207e-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2207e-123">Example</span></span>

<span data-ttu-id="2207e-124">ICE70 notifica los siguientes errores para el ejemplo dado.</span><span class="sxs-lookup"><span data-stu-id="2207e-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="2207e-125">Para corregir este error: Si desea que el valor sea numérico, cambie el valor para usar todos los caracteres numéricos.</span><span class="sxs-lookup"><span data-stu-id="2207e-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="2207e-126">Si desea que el valor sea una cadena, debe ir precedido por dos ' \# ' ( \# \# ) en lugar de solo uno.</span><span class="sxs-lookup"><span data-stu-id="2207e-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="2207e-127">Para corregir este error: los caracteres hexadecimales válidos son 0-9, A-F y a-f.</span><span class="sxs-lookup"><span data-stu-id="2207e-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="2207e-128">Solo estos caracteres pueden seguir a \# x (o \# x).</span><span class="sxs-lookup"><span data-stu-id="2207e-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="2207e-129">[Tabla del registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="2207e-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="2207e-130">Registro</span><span class="sxs-lookup"><span data-stu-id="2207e-130">Registry</span></span> | <span data-ttu-id="2207e-131">Value</span><span class="sxs-lookup"><span data-stu-id="2207e-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="2207e-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="2207e-132">Reg1</span></span>     | <span data-ttu-id="2207e-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="2207e-133">\#12xz34</span></span> |
| <span data-ttu-id="2207e-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="2207e-134">Reg2</span></span>     | <span data-ttu-id="2207e-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="2207e-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="2207e-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2207e-136">Remarks</span></span>

-   <span data-ttu-id="2207e-137">\#\[Property \] es válido.</span><span class="sxs-lookup"><span data-stu-id="2207e-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="2207e-138">\#\[propiedad no válida (falta el corchete de cierre).</span><span class="sxs-lookup"><span data-stu-id="2207e-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="2207e-139">\#\[myprop1 \] \[ myprop2 es válido.</span><span class="sxs-lookup"><span data-stu-id="2207e-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="2207e-140">(Aunque en la última vez falta el corchete de cierre, myprop1 podría evaluarse como \# Str, por lo que tendría \# \# Str \[ myprop2, que es válido.</span><span class="sxs-lookup"><span data-stu-id="2207e-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="2207e-141">\#\]propiedad \[ no válida</span><span class="sxs-lookup"><span data-stu-id="2207e-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="2207e-142">Cualquier propiedad incrustada en una cadena de valor no puede estar en la \[ \] forma $compkey, \[ \# filekey \] o \[ ! filekey \] porque no son numéricas.</span><span class="sxs-lookup"><span data-stu-id="2207e-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="2207e-143">Sin embargo, hay una excepción, el \# \[ $compkey de propiedad \] \[ \] (o \[ \# filekey \] o \[ ! filekey \] ) es válido porque, como con el anterior, la \[ propiedad se \] puede evaluar como \# Str.</span><span class="sxs-lookup"><span data-stu-id="2207e-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2207e-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2207e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2207e-145">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="2207e-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



