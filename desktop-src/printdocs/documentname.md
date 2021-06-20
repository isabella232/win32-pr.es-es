---
description: Obtenga información sobre la propiedad DocumentName, que especifica un nombre descriptivo para el documento.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409278"
---
# <a name="documentname"></a><span data-ttu-id="ddf73-103">DocumentName</span><span class="sxs-lookup"><span data-stu-id="ddf73-103">DocumentName</span></span>

<span data-ttu-id="ddf73-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ddf73-104">This topic is not current.</span></span> <span data-ttu-id="ddf73-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ddf73-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ddf73-106">Especifica un nombre descriptivo para el documento.</span><span class="sxs-lookup"><span data-stu-id="ddf73-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="ddf73-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ddf73-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ddf73-108">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ddf73-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ddf73-109">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ddf73-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ddf73-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ddf73-110">Element Information</span></span>



| <span data-ttu-id="ddf73-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddf73-111">Name</span></span> | <span data-ttu-id="ddf73-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf73-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="ddf73-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ddf73-113">Element Type</span></span> <br/>   | <span data-ttu-id="ddf73-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ddf73-114">Property</span></span><br/> |
| <span data-ttu-id="ddf73-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ddf73-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ddf73-116">Documento</span><span class="sxs-lookup"><span data-stu-id="ddf73-116">Document</span></span><br/> |
| <span data-ttu-id="ddf73-117">Notas</span><span class="sxs-lookup"><span data-stu-id="ddf73-117">Notes</span></span> <br/>          | <span data-ttu-id="ddf73-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ddf73-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ddf73-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ddf73-119">Structural Content</span></span>

<span data-ttu-id="ddf73-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ddf73-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="ddf73-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="ddf73-121">Structure Variables</span></span>

<span data-ttu-id="ddf73-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ddf73-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ddf73-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddf73-123">Name</span></span>                             | <span data-ttu-id="ddf73-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ddf73-124">Data type</span></span>         | <span data-ttu-id="ddf73-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="ddf73-125">Unit</span></span> | <span data-ttu-id="ddf73-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="ddf73-126">Supported values</span></span> | <span data-ttu-id="ddf73-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="ddf73-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="ddf73-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="ddf73-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="ddf73-129">string</span><span class="sxs-lookup"><span data-stu-id="ddf73-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ddf73-130">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ddf73-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="ddf73-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddf73-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddf73-132">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ddf73-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




