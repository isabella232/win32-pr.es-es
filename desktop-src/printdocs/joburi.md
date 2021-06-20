---
description: Obtenga información sobre el elemento JobURI, que especifica un identificador uniforme de recursos (URI) para el documento.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408618"
---
# <a name="joburi"></a><span data-ttu-id="11c42-103">JobURI</span><span class="sxs-lookup"><span data-stu-id="11c42-103">JobURI</span></span>

<span data-ttu-id="11c42-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="11c42-104">This topic is not current.</span></span> <span data-ttu-id="11c42-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11c42-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11c42-106">Especifica un identificador uniforme de recursos (URI) para el documento.</span><span class="sxs-lookup"><span data-stu-id="11c42-106">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="11c42-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="11c42-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="11c42-108">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="11c42-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="11c42-109">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="11c42-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="11c42-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="11c42-110">Element Information</span></span>



| <span data-ttu-id="11c42-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="11c42-111">Name</span></span> | <span data-ttu-id="11c42-112">Valor</span><span class="sxs-lookup"><span data-stu-id="11c42-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="11c42-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="11c42-113">Element Type</span></span> <br/>   | <span data-ttu-id="11c42-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11c42-114">Property</span></span><br/> |
| <span data-ttu-id="11c42-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="11c42-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="11c42-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="11c42-116">Job</span></span><br/>      |
| <span data-ttu-id="11c42-117">Notas</span><span class="sxs-lookup"><span data-stu-id="11c42-117">Notes</span></span> <br/>          | <span data-ttu-id="11c42-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="11c42-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="11c42-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="11c42-119">Structural Content</span></span>

<span data-ttu-id="11c42-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="11c42-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="11c42-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="11c42-121">Structure Variables</span></span>

<span data-ttu-id="11c42-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="11c42-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="11c42-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="11c42-123">Name</span></span>                       | <span data-ttu-id="11c42-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="11c42-124">Data type</span></span>         | <span data-ttu-id="11c42-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="11c42-125">Unit</span></span> | <span data-ttu-id="11c42-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="11c42-126">Supported values</span></span> | <span data-ttu-id="11c42-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="11c42-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="11c42-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="11c42-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="11c42-129">string</span><span class="sxs-lookup"><span data-stu-id="11c42-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="11c42-130">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="11c42-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="11c42-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11c42-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c42-132">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="11c42-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




