---
description: ICE48 comprueba los directorios que están codificados de forma rígida en las rutas de acceso locales de la tabla de propiedades.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667751"
---
# <a name="ice48"></a><span data-ttu-id="fad5a-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="fad5a-103">ICE48</span></span>

<span data-ttu-id="fad5a-104">ICE48 comprueba los directorios que están codificados de forma rígida en las rutas de acceso locales de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="fad5a-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="fad5a-105">No codifique rutas de acceso de directorio a unidades locales porque los equipos difieren en la instalación de la unidad local.</span><span class="sxs-lookup"><span data-stu-id="fad5a-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="fad5a-106">Esta práctica puede ser aceptable si se implementa una aplicación en un gran número de equipos en los que las partes relevantes de las unidades son las mismas.</span><span class="sxs-lookup"><span data-stu-id="fad5a-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="fad5a-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="fad5a-107">Result</span></span>

<span data-ttu-id="fad5a-108">ICE48 envía un mensaje de error si hay un directorio codificado de forma rígida en una ruta de acceso local en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fad5a-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="fad5a-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fad5a-109">Example</span></span>

<span data-ttu-id="fad5a-110">ICE48 notificaría la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="fad5a-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="fad5a-111">[Tabla de directorio](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fad5a-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="fad5a-112">Directorio</span><span class="sxs-lookup"><span data-stu-id="fad5a-112">Directory</span></span> | <span data-ttu-id="fad5a-113">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="fad5a-113">Directory\_Parent</span></span> | <span data-ttu-id="fad5a-114">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="fad5a-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="fad5a-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="fad5a-115">Dir1</span></span>      |                   | <span data-ttu-id="fad5a-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="fad5a-116">SourceDir</span></span>  |



 

<span data-ttu-id="fad5a-117">[Tabla de propiedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fad5a-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="fad5a-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fad5a-118">Property</span></span> | <span data-ttu-id="fad5a-119">Value</span><span class="sxs-lookup"><span data-stu-id="fad5a-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="fad5a-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="fad5a-120">Dir1</span></span>     | <span data-ttu-id="fad5a-121">d: \\ origen</span><span class="sxs-lookup"><span data-stu-id="fad5a-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fad5a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fad5a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fad5a-123">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="fad5a-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



