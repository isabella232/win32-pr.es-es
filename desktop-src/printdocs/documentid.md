---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d41bb96fe904a80210a951f700830604030eadd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717409"
---
# <a name="documentid"></a><span data-ttu-id="7e531-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="7e531-104">DocumentID</span></span>

<span data-ttu-id="7e531-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="7e531-105">This topic is not current.</span></span> <span data-ttu-id="7e531-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7e531-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7e531-107">Especifica un identificador único para el documento.</span><span class="sxs-lookup"><span data-stu-id="7e531-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="7e531-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7e531-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7e531-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="7e531-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7e531-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="7e531-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7e531-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7e531-111">Element Information</span></span>



| <span data-ttu-id="7e531-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="7e531-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="7e531-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7e531-113">Element Type</span></span> <br/>   | <span data-ttu-id="7e531-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e531-114">Property</span></span><br/> |
| <span data-ttu-id="7e531-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7e531-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7e531-116">Documento</span><span class="sxs-lookup"><span data-stu-id="7e531-116">Document</span></span><br/> |
| <span data-ttu-id="7e531-117">Notas</span><span class="sxs-lookup"><span data-stu-id="7e531-117">Notes</span></span> <br/>          | <span data-ttu-id="7e531-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7e531-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7e531-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="7e531-119">Structural Content</span></span>

<span data-ttu-id="7e531-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e531-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="7e531-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="7e531-121">Structure Variables</span></span>

<span data-ttu-id="7e531-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7e531-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7e531-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="7e531-123">Name</span></span>                           | <span data-ttu-id="7e531-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7e531-124">Data type</span></span>         | <span data-ttu-id="7e531-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="7e531-125">Unit</span></span> | <span data-ttu-id="7e531-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="7e531-126">Supported values</span></span> | <span data-ttu-id="7e531-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="7e531-127">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="7e531-128">\_DocumentIDValue\_</span><span class="sxs-lookup"><span data-stu-id="7e531-128">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="7e531-129">string</span><span class="sxs-lookup"><span data-stu-id="7e531-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7e531-130">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="7e531-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="7e531-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e531-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e531-132">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7e531-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




