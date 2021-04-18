---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721365"
---
# <a name="jobname"></a><span data-ttu-id="41c5c-104">JobName</span><span class="sxs-lookup"><span data-stu-id="41c5c-104">JobName</span></span>

<span data-ttu-id="41c5c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="41c5c-105">This topic is not current.</span></span> <span data-ttu-id="41c5c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="41c5c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="41c5c-107">Especifica un nombre descriptivo para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="41c5c-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="41c5c-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="41c5c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="41c5c-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="41c5c-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="41c5c-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="41c5c-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="41c5c-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="41c5c-111">Element Information</span></span>



| <span data-ttu-id="41c5c-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="41c5c-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="41c5c-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="41c5c-113">Element Type</span></span> <br/>   | <span data-ttu-id="41c5c-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41c5c-114">Property</span></span><br/> |
| <span data-ttu-id="41c5c-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="41c5c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="41c5c-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="41c5c-116">Job</span></span><br/>      |
| <span data-ttu-id="41c5c-117">Notas</span><span class="sxs-lookup"><span data-stu-id="41c5c-117">Notes</span></span> <br/>          | <span data-ttu-id="41c5c-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="41c5c-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="41c5c-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="41c5c-119">Structural Content</span></span>

<span data-ttu-id="41c5c-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="41c5c-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="41c5c-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="41c5c-121">Structure Variables</span></span>

<span data-ttu-id="41c5c-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="41c5c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="41c5c-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="41c5c-123">Name</span></span>                        | <span data-ttu-id="41c5c-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="41c5c-124">Data type</span></span>         | <span data-ttu-id="41c5c-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="41c5c-125">Unit</span></span> | <span data-ttu-id="41c5c-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="41c5c-126">Supported values</span></span> | <span data-ttu-id="41c5c-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="41c5c-127">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="41c5c-128">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="41c5c-128">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="41c5c-129">string</span><span class="sxs-lookup"><span data-stu-id="41c5c-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="41c5c-130">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="41c5c-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="41c5c-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41c5c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41c5c-132">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="41c5c-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




