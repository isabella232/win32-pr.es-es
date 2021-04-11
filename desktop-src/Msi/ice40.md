---
description: ICE40 realiza una validación diversa.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156717"
---
# <a name="ice40"></a><span data-ttu-id="cd149-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="cd149-103">ICE40</span></span>

<span data-ttu-id="cd149-104">ICE40 realiza una validación diversa.</span><span class="sxs-lookup"><span data-stu-id="cd149-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="cd149-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="cd149-105">Result</span></span>

<span data-ttu-id="cd149-106">ICE40 expone advertencias en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cd149-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="cd149-107">Se ha invalidado la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="cd149-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="cd149-108">La [tabla RemoveIniFile](removeinifile-table.md) tiene una entrada de etiqueta DELETE sin ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cd149-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="cd149-109">Falta la [tabla de errores](error-table.md) en el archivo. msi y la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) es menor o igual que 100.</span><span class="sxs-lookup"><span data-stu-id="cd149-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="cd149-110">Esta advertencia de ICE está obsoleta porque Windows Installer no requiere que el paquete tenga una tabla de errores.</span><span class="sxs-lookup"><span data-stu-id="cd149-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="cd149-111">Los mensajes de error se pueden recuperar mediante Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="cd149-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="cd149-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd149-112">Example</span></span>

[<span data-ttu-id="cd149-113">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="cd149-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="cd149-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd149-114">Property</span></span>                               | <span data-ttu-id="cd149-115">Value</span><span class="sxs-lookup"><span data-stu-id="cd149-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="cd149-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="cd149-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="cd149-117">A</span><span class="sxs-lookup"><span data-stu-id="cd149-117">A</span></span>     |



 

[<span data-ttu-id="cd149-118">Tabla RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="cd149-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="cd149-119">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="cd149-119">RemoveIniFile</span></span>                          | <span data-ttu-id="cd149-120">Acción</span><span class="sxs-lookup"><span data-stu-id="cd149-120">Action</span></span> | <span data-ttu-id="cd149-121">Value</span><span class="sxs-lookup"><span data-stu-id="cd149-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="cd149-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="cd149-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="cd149-123">4</span><span class="sxs-lookup"><span data-stu-id="cd149-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="cd149-124">Results</span><span class="sxs-lookup"><span data-stu-id="cd149-124">Results</span></span>

<span data-ttu-id="cd149-125">ICE40 notificaría los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="cd149-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="cd149-126">Error ICE40</span><span class="sxs-lookup"><span data-stu-id="cd149-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="cd149-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd149-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd149-128">[**REINSTALLMODE**](reinstallmode.md) se define en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd149-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="cd149-129">Esto puede producir dificultades.</span><span class="sxs-lookup"><span data-stu-id="cd149-129">This may cause difficulties.</span></span> | <span data-ttu-id="cd149-130">La definición de la propiedad [**REINSTALLMODE**](reinstallmode.md) en el archivo. msi puede provocar un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="cd149-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="cd149-131">Para corregir este error, no defina esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cd149-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cd149-132">La entrada RemoveIniFile Remove1 debe tener un valor, porque la acción es "eliminar etiqueta" (4).</span><span class="sxs-lookup"><span data-stu-id="cd149-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="cd149-133">Hay una acción de eliminación de etiqueta en la columna RemoveIniFile de la [tabla RemoveIniFile](removeinifile-table.md) sin especificar la etiqueta que se va a eliminar en la columna valor.</span><span class="sxs-lookup"><span data-stu-id="cd149-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cd149-134">Falta la tabla de errores.</span><span class="sxs-lookup"><span data-stu-id="cd149-134">Error Table is missing.</span></span> <span data-ttu-id="cd149-135">Solo se generarán mensajes de error numéricos.</span><span class="sxs-lookup"><span data-stu-id="cd149-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="cd149-136">Esta advertencia de ICE está obsoleta porque Windows Installer no requiere que el paquete tenga una [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd149-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="cd149-137">Los mensajes de error se pueden recuperar mediante Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="cd149-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="cd149-138">Esta ADVERTENCIA significa que en el archivo. msi falta la [tabla de errores](error-table.md) y la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) es menor o igual que 100.</span><span class="sxs-lookup"><span data-stu-id="cd149-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="cd149-139">Para corregir este error, use una versión actual del Windows Installer o agregue una tabla de errores al paquete de instalación y plantillas de formato de autor en la columna mensaje para los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="cd149-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="cd149-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd149-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd149-141">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="cd149-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




