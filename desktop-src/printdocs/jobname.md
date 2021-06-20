---
description: Obtenga información sobre el elemento JobName, que especifica un nombre descriptivo para el trabajo. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfb63a54e9501ff5dc45ff09a925396c168b20c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408878"
---
# <a name="jobname"></a><span data-ttu-id="d9094-104">JobName</span><span class="sxs-lookup"><span data-stu-id="d9094-104">JobName</span></span>

<span data-ttu-id="d9094-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d9094-105">This topic is not current.</span></span> <span data-ttu-id="d9094-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d9094-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d9094-107">Especifica un nombre descriptivo para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d9094-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="d9094-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d9094-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d9094-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d9094-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d9094-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d9094-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d9094-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d9094-111">Element Information</span></span>



| <span data-ttu-id="d9094-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9094-112">Name</span></span> | <span data-ttu-id="d9094-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d9094-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="d9094-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d9094-114">Element Type</span></span> <br/>   | <span data-ttu-id="d9094-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9094-115">Property</span></span><br/> |
| <span data-ttu-id="d9094-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d9094-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d9094-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="d9094-117">Job</span></span><br/>      |
| <span data-ttu-id="d9094-118">Notas</span><span class="sxs-lookup"><span data-stu-id="d9094-118">Notes</span></span> <br/>          | <span data-ttu-id="d9094-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d9094-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d9094-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d9094-120">Structural Content</span></span>

<span data-ttu-id="d9094-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d9094-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d9094-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="d9094-122">Structure Variables</span></span>

<span data-ttu-id="d9094-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d9094-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d9094-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9094-124">Name</span></span>                        | <span data-ttu-id="d9094-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d9094-125">Data type</span></span>         | <span data-ttu-id="d9094-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="d9094-126">Unit</span></span> | <span data-ttu-id="d9094-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="d9094-127">Supported values</span></span> | <span data-ttu-id="d9094-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="d9094-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="d9094-129">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="d9094-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="d9094-130">string</span><span class="sxs-lookup"><span data-stu-id="d9094-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d9094-131">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d9094-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="d9094-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9094-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9094-133">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d9094-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




