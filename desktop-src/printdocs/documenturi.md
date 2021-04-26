---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d339b1b469f276492f7989b0ed7951ca1edad8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997072"
---
# <a name="documenturi"></a><span data-ttu-id="2e3a6-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="2e3a6-104">DocumentURI</span></span>

<span data-ttu-id="2e3a6-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-105">This topic is not current.</span></span> <span data-ttu-id="2e3a6-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e3a6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e3a6-107">Especifica un identificador uniforme de recursos (URI) para el documento.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="2e3a6-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2e3a6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2e3a6-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="2e3a6-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2e3a6-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2e3a6-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2e3a6-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2e3a6-111">Element Information</span></span>



| <span data-ttu-id="2e3a6-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="2e3a6-112">Name</span></span> | <span data-ttu-id="2e3a6-113">Value</span><span class="sxs-lookup"><span data-stu-id="2e3a6-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="2e3a6-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2e3a6-114">Element Type</span></span> <br/>   | <span data-ttu-id="2e3a6-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2e3a6-115">Property</span></span><br/> |
| <span data-ttu-id="2e3a6-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2e3a6-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2e3a6-117">Documento</span><span class="sxs-lookup"><span data-stu-id="2e3a6-117">Document</span></span><br/> |
| <span data-ttu-id="2e3a6-118">Notas</span><span class="sxs-lookup"><span data-stu-id="2e3a6-118">Notes</span></span> <br/>          | <span data-ttu-id="2e3a6-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2e3a6-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="2e3a6-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="2e3a6-120">Structural Content</span></span>

<span data-ttu-id="2e3a6-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2e3a6-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="2e3a6-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="2e3a6-122">Structure Variables</span></span>

<span data-ttu-id="2e3a6-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2e3a6-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="2e3a6-124">Name</span></span>                            | <span data-ttu-id="2e3a6-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2e3a6-125">Data type</span></span>         | <span data-ttu-id="2e3a6-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="2e3a6-126">Unit</span></span> | <span data-ttu-id="2e3a6-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="2e3a6-127">Supported values</span></span> | <span data-ttu-id="2e3a6-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="2e3a6-128">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="2e3a6-129">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="2e3a6-129">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="2e3a6-130">string</span><span class="sxs-lookup"><span data-stu-id="2e3a6-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2e3a6-131">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2e3a6-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2e3a6-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e3a6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e3a6-133">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2e3a6-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




