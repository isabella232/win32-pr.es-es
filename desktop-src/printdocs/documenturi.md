---
description: Obtenga información sobre la propiedad DocumentURI. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548813"
---
# <a name="documenturi"></a><span data-ttu-id="34a35-105">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="34a35-105">DocumentURI</span></span>

<span data-ttu-id="34a35-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="34a35-106">This topic is not current.</span></span> <span data-ttu-id="34a35-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="34a35-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="34a35-108">Especifica un identificador uniforme de recursos (URI) para el documento.</span><span class="sxs-lookup"><span data-stu-id="34a35-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="34a35-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="34a35-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="34a35-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="34a35-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="34a35-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="34a35-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="34a35-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="34a35-112">Element Information</span></span>



| <span data-ttu-id="34a35-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="34a35-113">Name</span></span> | <span data-ttu-id="34a35-114">Valor</span><span class="sxs-lookup"><span data-stu-id="34a35-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="34a35-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="34a35-115">Element Type</span></span> <br/>   | <span data-ttu-id="34a35-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34a35-116">Property</span></span><br/> |
| <span data-ttu-id="34a35-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="34a35-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="34a35-118">Documento</span><span class="sxs-lookup"><span data-stu-id="34a35-118">Document</span></span><br/> |
| <span data-ttu-id="34a35-119">Notas</span><span class="sxs-lookup"><span data-stu-id="34a35-119">Notes</span></span> <br/>          | <span data-ttu-id="34a35-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="34a35-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="34a35-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="34a35-121">Structural Content</span></span>

<span data-ttu-id="34a35-122">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="34a35-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="34a35-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="34a35-123">Structure Variables</span></span>

<span data-ttu-id="34a35-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="34a35-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="34a35-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="34a35-125">Name</span></span>                            | <span data-ttu-id="34a35-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="34a35-126">Data type</span></span>         | <span data-ttu-id="34a35-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="34a35-127">Unit</span></span> | <span data-ttu-id="34a35-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="34a35-128">Supported values</span></span> | <span data-ttu-id="34a35-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="34a35-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="34a35-130">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="34a35-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="34a35-131">string</span><span class="sxs-lookup"><span data-stu-id="34a35-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="34a35-132">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="34a35-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="34a35-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34a35-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a35-134">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="34a35-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




