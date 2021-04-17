---
description: ICE65 comprueba que la tabla de entorno no tiene valores de prefijo o de anexión no válidos.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652997"
---
# <a name="ice65"></a><span data-ttu-id="af2f3-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="af2f3-103">ICE65</span></span>

<span data-ttu-id="af2f3-104">ICE65 comprueba que la [tabla de entorno](environment-table.md) no tiene valores de prefijo o de anexión no válidos.</span><span class="sxs-lookup"><span data-stu-id="af2f3-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="af2f3-105">Si no se corrige una advertencia o un error informados por ICE65, generalmente se producen problemas en la instalación, desinstalación o reparación de la variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="af2f3-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="af2f3-106">Por ejemplo, solo se pueden quitar algunos valores de una variable determinada si uno o varios de los valores de esa variable tienen un separador final.</span><span class="sxs-lookup"><span data-stu-id="af2f3-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="af2f3-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="af2f3-107">Result</span></span>

<span data-ttu-id="af2f3-108">ICE65 envía una advertencia o un error si la tabla de entorno tiene valores de prefijo o de anexión no válidos.</span><span class="sxs-lookup"><span data-stu-id="af2f3-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="af2f3-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af2f3-109">Example</span></span>

<span data-ttu-id="af2f3-110">ICE65 notifica el siguiente error y advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="af2f3-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="af2f3-111">El valor null final al final del valor ( \[ ~ \] ) marca este valor para que se antepone a cualquier valor existente.</span><span class="sxs-lookup"><span data-stu-id="af2f3-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="af2f3-112">El carácter que precede a null (un punto y coma) se convierte en el separador de este valor.</span><span class="sxs-lookup"><span data-stu-id="af2f3-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="af2f3-113">Este valor tiene un punto y coma al principio de la cadena.</span><span class="sxs-lookup"><span data-stu-id="af2f3-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="af2f3-114">Para corregir este error, simplemente elimine el punto y coma inicial.</span><span class="sxs-lookup"><span data-stu-id="af2f3-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="af2f3-115">El valor null inicial en el valor ( \[ ~ \] ) marca este valor para anexarlo a cualquier valor existente.</span><span class="sxs-lookup"><span data-stu-id="af2f3-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="af2f3-116">El carácter situado inmediatamente después de la NULL se convierte en el separador de este valor.</span><span class="sxs-lookup"><span data-stu-id="af2f3-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="af2f3-117">En este caso, ese carácter es la letra "e", que también se produce en medio de la cadena que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="af2f3-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="af2f3-118">Esta condición (con un separador que sea igual que un carácter dentro de la cadena que se va a anexar) puede producir resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="af2f3-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="af2f3-119">La letra "e", que es una letra común, es probable que se encuentre en el valor.</span><span class="sxs-lookup"><span data-stu-id="af2f3-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="af2f3-120">Una opción mejor sería ";" u otros caracteres no alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="af2f3-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="af2f3-121">(Sin embargo, si el valor es una ruta de acceso, ":" y " \\ " y "." son opciones de riesgo).</span><span class="sxs-lookup"><span data-stu-id="af2f3-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="af2f3-122">Para corregir esta advertencia, use un carácter separador diferente.</span><span class="sxs-lookup"><span data-stu-id="af2f3-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="af2f3-123">Tabla de entorno</span><span class="sxs-lookup"><span data-stu-id="af2f3-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="af2f3-124">Componente</span><span class="sxs-lookup"><span data-stu-id="af2f3-124">Component</span></span> | <span data-ttu-id="af2f3-125">Directorio</span><span class="sxs-lookup"><span data-stu-id="af2f3-125">Directory</span></span> | <span data-ttu-id="af2f3-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="af2f3-126">Attributes</span></span>         | <span data-ttu-id="af2f3-127">Rutas</span><span class="sxs-lookup"><span data-stu-id="af2f3-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="af2f3-128">Var1</span><span class="sxs-lookup"><span data-stu-id="af2f3-128">Var1</span></span>      | <span data-ttu-id="af2f3-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="af2f3-129">TestVar</span></span>   | <span data-ttu-id="af2f3-130">\[~\]; AppendThis</span><span class="sxs-lookup"><span data-stu-id="af2f3-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="af2f3-131">TestComponent</span><span class="sxs-lookup"><span data-stu-id="af2f3-131">TestComponent</span></span> |
| <span data-ttu-id="af2f3-132">Var2</span><span class="sxs-lookup"><span data-stu-id="af2f3-132">Var2</span></span>      | <span data-ttu-id="af2f3-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="af2f3-133">TestVar</span></span>   | <span data-ttu-id="af2f3-134">\[~\]eAppendThis</span><span class="sxs-lookup"><span data-stu-id="af2f3-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="af2f3-135">TestComponent</span><span class="sxs-lookup"><span data-stu-id="af2f3-135">TestComponent</span></span> |
| <span data-ttu-id="af2f3-136">Var3</span><span class="sxs-lookup"><span data-stu-id="af2f3-136">Var3</span></span>      | <span data-ttu-id="af2f3-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="af2f3-137">TestVar</span></span>   | <span data-ttu-id="af2f3-138">; PrependThis;\[~\]</span><span class="sxs-lookup"><span data-stu-id="af2f3-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="af2f3-139">TestComponent</span><span class="sxs-lookup"><span data-stu-id="af2f3-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="af2f3-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af2f3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2f3-141">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="af2f3-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



