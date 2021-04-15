---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105649331"
---
# <a name="jobid"></a><span data-ttu-id="a8a3b-104">JobID</span><span class="sxs-lookup"><span data-stu-id="a8a3b-104">JobID</span></span>

<span data-ttu-id="a8a3b-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-105">This topic is not current.</span></span> <span data-ttu-id="a8a3b-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a8a3b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8a3b-107">Especifica un identificador único para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="a8a3b-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a8a3b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a8a3b-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="a8a3b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a8a3b-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="a8a3b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a8a3b-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a8a3b-111">Element Information</span></span>



| <span data-ttu-id="a8a3b-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8a3b-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="a8a3b-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a8a3b-113">Element Type</span></span> <br/>   | <span data-ttu-id="a8a3b-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8a3b-114">Property</span></span><br/> |
| <span data-ttu-id="a8a3b-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="a8a3b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a8a3b-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="a8a3b-116">Job</span></span><br/>      |
| <span data-ttu-id="a8a3b-117">Notas</span><span class="sxs-lookup"><span data-stu-id="a8a3b-117">Notes</span></span> <br/>          | <span data-ttu-id="a8a3b-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a8a3b-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="a8a3b-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="a8a3b-119">Structural Content</span></span>

<span data-ttu-id="a8a3b-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="a8a3b-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="a8a3b-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="a8a3b-121">Structure Variables</span></span>

<span data-ttu-id="a8a3b-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a8a3b-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8a3b-123">Name</span></span>                      | <span data-ttu-id="a8a3b-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a8a3b-124">Data type</span></span>         | <span data-ttu-id="a8a3b-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="a8a3b-125">Unit</span></span> | <span data-ttu-id="a8a3b-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="a8a3b-126">Supported values</span></span> | <span data-ttu-id="a8a3b-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="a8a3b-127">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="a8a3b-128">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="a8a3b-128">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="a8a3b-129">string</span><span class="sxs-lookup"><span data-stu-id="a8a3b-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a8a3b-130">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="a8a3b-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="a8a3b-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8a3b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8a3b-132">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="a8a3b-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




