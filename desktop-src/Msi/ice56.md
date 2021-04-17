---
description: ICE56 valida que la estructura de directorios del archivo. msi tiene un único directorio raíz, que la raíz es la propiedad TARGETDIR y que el valor de la propiedad SourceDir está en la columna DefaultDir de la tabla de directorio.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668129"
---
# <a name="ice56"></a><span data-ttu-id="85185-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="85185-103">ICE56</span></span>

<span data-ttu-id="85185-104">ICE56 valida que la estructura de directorios del archivo. msi tiene un único directorio raíz, que la raíz es la propiedad [**targetDir**](targetdir.md) y que el valor de la propiedad [**SourceDir**](sourcedir.md) está en la columna DefaultDir de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="85185-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="85185-105">Si un archivo. msi tiene varias raíces o especifica una raíz distinta de [**targetDir**](targetdir.md), una [instalación administrativa](administrative-installation.md) no crea una imagen administrativa correcta.</span><span class="sxs-lookup"><span data-stu-id="85185-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="85185-106">Tenga en cuenta que los directorios vacíos no se comprueban con ICE56.</span><span class="sxs-lookup"><span data-stu-id="85185-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="85185-107">La estructura de directorios pasa la validación con varios directorios raíz si los directorios adicionales están vacíos.</span><span class="sxs-lookup"><span data-stu-id="85185-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="85185-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="85185-108">Result</span></span>

<span data-ttu-id="85185-109">ICE56 publica un error si el archivo. msi no tiene una sola raíz, [**targetDir**](targetdir.md)o si [**SourceDir**](sourcedir.md) no se especifica en la columna DefaultDir de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="85185-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="85185-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85185-110">Example</span></span>

<span data-ttu-id="85185-111">ICE56 notifica los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="85185-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="85185-112">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="85185-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="85185-113">Directorio</span><span class="sxs-lookup"><span data-stu-id="85185-113">Directory</span></span> | <span data-ttu-id="85185-114">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="85185-114">Directory\_Parent</span></span> | <span data-ttu-id="85185-115">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="85185-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="85185-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="85185-116">TARGETDIR</span></span> |                   | <span data-ttu-id="85185-117">Temp</span><span class="sxs-lookup"><span data-stu-id="85185-117">Temp</span></span>       |
| <span data-ttu-id="85185-118">Root2</span><span class="sxs-lookup"><span data-stu-id="85185-118">Root2</span></span>     | <span data-ttu-id="85185-119">Root2</span><span class="sxs-lookup"><span data-stu-id="85185-119">Root2</span></span>             | <span data-ttu-id="85185-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="85185-120">SourceDir</span></span>  |



 

<span data-ttu-id="85185-121">Para corregir el primer error, la raíz de [**targetDir**](targetdir.md) debe tener un valor de DefaultDir de [**SourceDir**](sourcedir.md).</span><span class="sxs-lookup"><span data-stu-id="85185-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="85185-122">También se acepta SOURCEDIR.</span><span class="sxs-lookup"><span data-stu-id="85185-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="85185-123">Puede convertir el **targetDir** en el elemento primario de la segunda raíz y usar el valor '. ' en la columna DefaultDir.</span><span class="sxs-lookup"><span data-stu-id="85185-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="85185-124">Vea la [tabla de directorios](directory-table.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="85185-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="85185-125">Para corregir el segundo error, la estructura de directorios solo debe tener una raíz denominada [**targetDir**](targetdir.md).</span><span class="sxs-lookup"><span data-stu-id="85185-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85185-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85185-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85185-127">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="85185-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



