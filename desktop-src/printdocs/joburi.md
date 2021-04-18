---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698019"
---
# <a name="joburi"></a><span data-ttu-id="53f2f-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="53f2f-104">JobURI</span></span>

<span data-ttu-id="53f2f-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="53f2f-105">This topic is not current.</span></span> <span data-ttu-id="53f2f-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="53f2f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="53f2f-107">Especifica un identificador uniforme de recursos (URI) para el documento.</span><span class="sxs-lookup"><span data-stu-id="53f2f-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="53f2f-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="53f2f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="53f2f-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="53f2f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="53f2f-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="53f2f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="53f2f-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="53f2f-111">Element Information</span></span>



| <span data-ttu-id="53f2f-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="53f2f-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="53f2f-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="53f2f-113">Element Type</span></span> <br/>   | <span data-ttu-id="53f2f-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53f2f-114">Property</span></span><br/> |
| <span data-ttu-id="53f2f-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="53f2f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="53f2f-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="53f2f-116">Job</span></span><br/>      |
| <span data-ttu-id="53f2f-117">Notas</span><span class="sxs-lookup"><span data-stu-id="53f2f-117">Notes</span></span> <br/>          | <span data-ttu-id="53f2f-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="53f2f-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="53f2f-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="53f2f-119">Structural Content</span></span>

<span data-ttu-id="53f2f-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="53f2f-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="53f2f-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="53f2f-121">Structure Variables</span></span>

<span data-ttu-id="53f2f-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="53f2f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="53f2f-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="53f2f-123">Name</span></span>                       | <span data-ttu-id="53f2f-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="53f2f-124">Data type</span></span>         | <span data-ttu-id="53f2f-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="53f2f-125">Unit</span></span> | <span data-ttu-id="53f2f-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="53f2f-126">Supported values</span></span> | <span data-ttu-id="53f2f-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="53f2f-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="53f2f-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="53f2f-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="53f2f-129">string</span><span class="sxs-lookup"><span data-stu-id="53f2f-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="53f2f-130">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="53f2f-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="53f2f-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53f2f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53f2f-132">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="53f2f-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




