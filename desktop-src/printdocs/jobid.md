---
description: Obtenga información sobre el elemento JobID, que especifica un identificador único para el trabajo. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408888"
---
# <a name="jobid"></a><span data-ttu-id="7bd9d-104">JobID</span><span class="sxs-lookup"><span data-stu-id="7bd9d-104">JobID</span></span>

<span data-ttu-id="7bd9d-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-105">This topic is not current.</span></span> <span data-ttu-id="7bd9d-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7bd9d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7bd9d-107">Especifica un identificador único para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="7bd9d-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7bd9d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7bd9d-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="7bd9d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7bd9d-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7bd9d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7bd9d-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7bd9d-111">Element Information</span></span>



| <span data-ttu-id="7bd9d-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="7bd9d-112">Name</span></span> | <span data-ttu-id="7bd9d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7bd9d-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="7bd9d-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7bd9d-114">Element Type</span></span> <br/>   | <span data-ttu-id="7bd9d-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7bd9d-115">Property</span></span><br/> |
| <span data-ttu-id="7bd9d-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7bd9d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7bd9d-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="7bd9d-117">Job</span></span><br/>      |
| <span data-ttu-id="7bd9d-118">Notas</span><span class="sxs-lookup"><span data-stu-id="7bd9d-118">Notes</span></span> <br/>          | <span data-ttu-id="7bd9d-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7bd9d-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7bd9d-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="7bd9d-120">Structural Content</span></span>

<span data-ttu-id="7bd9d-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="7bd9d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="7bd9d-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="7bd9d-122">Structure Variables</span></span>

<span data-ttu-id="7bd9d-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7bd9d-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="7bd9d-124">Name</span></span>                      | <span data-ttu-id="7bd9d-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7bd9d-125">Data type</span></span>         | <span data-ttu-id="7bd9d-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="7bd9d-126">Unit</span></span> | <span data-ttu-id="7bd9d-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="7bd9d-127">Supported values</span></span> | <span data-ttu-id="7bd9d-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="7bd9d-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="7bd9d-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="7bd9d-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="7bd9d-130">string</span><span class="sxs-lookup"><span data-stu-id="7bd9d-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7bd9d-131">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7bd9d-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="7bd9d-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bd9d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bd9d-133">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7bd9d-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




