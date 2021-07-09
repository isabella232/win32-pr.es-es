---
description: Obtenga información sobre el elemento configurable por el usuario JobHolePunch. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549363"
---
# <a name="jobholepunch"></a><span data-ttu-id="41790-105">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="41790-105">JobHolePunch</span></span>

<span data-ttu-id="41790-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="41790-106">This topic is not current.</span></span> <span data-ttu-id="41790-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="41790-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="41790-108">Describe las características de los huecos de la salida.</span><span class="sxs-lookup"><span data-stu-id="41790-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="41790-109">Todos los documentos se reúnen.</span><span class="sxs-lookup"><span data-stu-id="41790-109">All documents are punched together.</span></span> <span data-ttu-id="41790-110">Las palabras clave JobHolePunch y DocumentHolePunch son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="41790-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="41790-111">Ambos no deben especificarse simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="41790-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="41790-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="41790-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="41790-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="41790-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="41790-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="41790-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="41790-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="41790-115">Element Information</span></span>



| <span data-ttu-id="41790-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="41790-116">Name</span></span> | <span data-ttu-id="41790-117">Valor</span><span class="sxs-lookup"><span data-stu-id="41790-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41790-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="41790-118">Element Type</span></span> <br/>   | <span data-ttu-id="41790-119">Característica</span><span class="sxs-lookup"><span data-stu-id="41790-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="41790-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="41790-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="41790-121">Trabajo</span><span class="sxs-lookup"><span data-stu-id="41790-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="41790-122">Notas</span><span class="sxs-lookup"><span data-stu-id="41790-122">Notes</span></span> <br/>          | <span data-ttu-id="41790-123">Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica mediante el origen del eje X y el eje Y.</span><span class="sxs-lookup"><span data-stu-id="41790-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="41790-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="41790-124">Structural Content</span></span>

<span data-ttu-id="41790-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="41790-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="41790-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="41790-126">Structure Variables</span></span>

<span data-ttu-id="41790-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="41790-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="41790-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="41790-128">Name</span></span>                               | <span data-ttu-id="41790-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="41790-129">Data type</span></span>         | <span data-ttu-id="41790-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="41790-130">Unit</span></span>                  | <span data-ttu-id="41790-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="41790-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="41790-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="41790-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="41790-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="41790-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="41790-134">string</span><span class="sxs-lookup"><span data-stu-id="41790-134">string</span></span><br/> | <span data-ttu-id="41790-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="41790-135">characters</span></span><br/> | <span data-ttu-id="41790-136">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="41790-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="41790-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="41790-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="41790-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="41790-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="41790-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="41790-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="41790-140">string</span><span class="sxs-lookup"><span data-stu-id="41790-140">string</span></span><br/> | <span data-ttu-id="41790-141">N/D</span><span class="sxs-lookup"><span data-stu-id="41790-141">n/a</span></span><br/>        | <span data-ttu-id="41790-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="41790-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="41790-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="41790-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="41790-144">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="41790-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="41790-145">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="41790-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="41790-146">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="41790-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="41790-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41790-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41790-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="41790-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




