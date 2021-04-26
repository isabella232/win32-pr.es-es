---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2d77d185ab7edc611a82f94a2ce92428d9f167
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998142"
---
# <a name="jobid"></a><span data-ttu-id="51562-104">JobID</span><span class="sxs-lookup"><span data-stu-id="51562-104">JobID</span></span>

<span data-ttu-id="51562-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="51562-105">This topic is not current.</span></span> <span data-ttu-id="51562-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="51562-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="51562-107">Especifica un identificador único para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="51562-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="51562-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="51562-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="51562-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="51562-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="51562-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="51562-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="51562-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="51562-111">Element Information</span></span>



| <span data-ttu-id="51562-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="51562-112">Name</span></span> | <span data-ttu-id="51562-113">Value</span><span class="sxs-lookup"><span data-stu-id="51562-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="51562-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="51562-114">Element Type</span></span> <br/>   | <span data-ttu-id="51562-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51562-115">Property</span></span><br/> |
| <span data-ttu-id="51562-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="51562-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="51562-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="51562-117">Job</span></span><br/>      |
| <span data-ttu-id="51562-118">Notas</span><span class="sxs-lookup"><span data-stu-id="51562-118">Notes</span></span> <br/>          | <span data-ttu-id="51562-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="51562-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="51562-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="51562-120">Structural Content</span></span>

<span data-ttu-id="51562-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="51562-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="51562-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="51562-122">Structure Variables</span></span>

<span data-ttu-id="51562-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="51562-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="51562-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="51562-124">Name</span></span>                      | <span data-ttu-id="51562-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="51562-125">Data type</span></span>         | <span data-ttu-id="51562-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="51562-126">Unit</span></span> | <span data-ttu-id="51562-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="51562-127">Supported values</span></span> | <span data-ttu-id="51562-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="51562-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="51562-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="51562-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="51562-130">string</span><span class="sxs-lookup"><span data-stu-id="51562-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="51562-131">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="51562-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="51562-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51562-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51562-133">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="51562-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




