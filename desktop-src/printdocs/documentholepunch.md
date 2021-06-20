---
description: Obtenga información sobre el elemento DocumentHolePunch, que describe las características de los huecos de la salida.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409298"
---
# <a name="documentholepunch"></a><span data-ttu-id="15cd7-103">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="15cd7-103">DocumentHolePunch</span></span>

<span data-ttu-id="15cd7-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="15cd7-104">This topic is not current.</span></span> <span data-ttu-id="15cd7-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="15cd7-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15cd7-106">Describe las características de los huecos de la salida.</span><span class="sxs-lookup"><span data-stu-id="15cd7-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="15cd7-107">Cada documento se asecha por separado.</span><span class="sxs-lookup"><span data-stu-id="15cd7-107">Each document is punched separately.</span></span> <span data-ttu-id="15cd7-108">Las palabras clave JobHolePunch y DocumentHolePunch son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="15cd7-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="15cd7-109">Ambos no se deben especificar simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="15cd7-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="15cd7-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="15cd7-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="15cd7-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="15cd7-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="15cd7-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="15cd7-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="15cd7-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="15cd7-113">Element Information</span></span>



| <span data-ttu-id="15cd7-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="15cd7-114">Name</span></span> | <span data-ttu-id="15cd7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="15cd7-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="15cd7-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="15cd7-116">Element Type</span></span> <br/>   | <span data-ttu-id="15cd7-117">Característica</span><span class="sxs-lookup"><span data-stu-id="15cd7-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="15cd7-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="15cd7-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15cd7-119">Documento</span><span class="sxs-lookup"><span data-stu-id="15cd7-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="15cd7-120">Notas</span><span class="sxs-lookup"><span data-stu-id="15cd7-120">Notes</span></span> <br/>          | <span data-ttu-id="15cd7-121">Top, Bottom, Left y Right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="15cd7-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="15cd7-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="15cd7-122">Structural Content</span></span>

<span data-ttu-id="15cd7-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="15cd7-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="15cd7-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="15cd7-124">Structure Variables</span></span>

<span data-ttu-id="15cd7-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="15cd7-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15cd7-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="15cd7-126">Name</span></span>                               | <span data-ttu-id="15cd7-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="15cd7-127">Data type</span></span>         | <span data-ttu-id="15cd7-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="15cd7-128">Unit</span></span>                  | <span data-ttu-id="15cd7-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="15cd7-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="15cd7-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="15cd7-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="15cd7-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="15cd7-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="15cd7-132">string</span><span class="sxs-lookup"><span data-stu-id="15cd7-132">string</span></span><br/> | <span data-ttu-id="15cd7-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="15cd7-133">characters</span></span><br/> | <span data-ttu-id="15cd7-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="15cd7-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="15cd7-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="15cd7-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="15cd7-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="15cd7-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="15cd7-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="15cd7-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="15cd7-138">string</span><span class="sxs-lookup"><span data-stu-id="15cd7-138">string</span></span><br/> | <span data-ttu-id="15cd7-139">N/D</span><span class="sxs-lookup"><span data-stu-id="15cd7-139">n/a</span></span><br/>        | <span data-ttu-id="15cd7-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="15cd7-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="15cd7-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="15cd7-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="15cd7-142">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="15cd7-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="15cd7-143">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="15cd7-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="15cd7-144">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="15cd7-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="15cd7-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15cd7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15cd7-146">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="15cd7-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




