---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66809ef18edb7aa313ea5218f9122acf4ddd1ee8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997802"
---
# <a name="documentname"></a><span data-ttu-id="214e4-104">DocumentName</span><span class="sxs-lookup"><span data-stu-id="214e4-104">DocumentName</span></span>

<span data-ttu-id="214e4-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="214e4-105">This topic is not current.</span></span> <span data-ttu-id="214e4-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="214e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="214e4-107">Especifica un nombre descriptivo para el documento.</span><span class="sxs-lookup"><span data-stu-id="214e4-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="214e4-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="214e4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="214e4-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="214e4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="214e4-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="214e4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="214e4-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="214e4-111">Element Information</span></span>



| <span data-ttu-id="214e4-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="214e4-112">Name</span></span> | <span data-ttu-id="214e4-113">Value</span><span class="sxs-lookup"><span data-stu-id="214e4-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="214e4-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="214e4-114">Element Type</span></span> <br/>   | <span data-ttu-id="214e4-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="214e4-115">Property</span></span><br/> |
| <span data-ttu-id="214e4-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="214e4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="214e4-117">Documento</span><span class="sxs-lookup"><span data-stu-id="214e4-117">Document</span></span><br/> |
| <span data-ttu-id="214e4-118">Notas</span><span class="sxs-lookup"><span data-stu-id="214e4-118">Notes</span></span> <br/>          | <span data-ttu-id="214e4-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="214e4-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="214e4-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="214e4-120">Structural Content</span></span>

<span data-ttu-id="214e4-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="214e4-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="214e4-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="214e4-122">Structure Variables</span></span>

<span data-ttu-id="214e4-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="214e4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="214e4-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="214e4-124">Name</span></span>                             | <span data-ttu-id="214e4-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="214e4-125">Data type</span></span>         | <span data-ttu-id="214e4-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="214e4-126">Unit</span></span> | <span data-ttu-id="214e4-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="214e4-127">Supported values</span></span> | <span data-ttu-id="214e4-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="214e4-128">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="214e4-129">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="214e4-129">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="214e4-130">string</span><span class="sxs-lookup"><span data-stu-id="214e4-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="214e4-131">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="214e4-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="214e4-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="214e4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="214e4-133">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="214e4-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




