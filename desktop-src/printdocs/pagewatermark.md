---
description: Obtenga información sobre el elemento PageWatermark configurable por el usuario. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b93eadfb3aeaa2c0be1de2cf5775bd1b5c88666
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396090"
---
# <a name="pagewatermark"></a><span data-ttu-id="5bb3e-105">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="5bb3e-105">PageWatermark</span></span>

<span data-ttu-id="5bb3e-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-106">This topic is not current.</span></span> <span data-ttu-id="5bb3e-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5bb3e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5bb3e-108">Describe la configuración de marca de agua de la salida y las características de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-108">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="5bb3e-109">Las marcas de agua se aplican a la página lógica, no a la página física.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-109">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="5bb3e-110">Por ejemplo, si DocumentDuplex está habilitado, aparecerá una marca de agua en cada página NUp de cada hoja.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-110">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="5bb3e-111">Si DocumentDuplex, PagesPerSheet=2, cada hoja tendrá 2 marcas de agua.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-111">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="5bb3e-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5bb3e-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5bb3e-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="5bb3e-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5bb3e-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5bb3e-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5bb3e-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5bb3e-115">Element Information</span></span>



| <span data-ttu-id="5bb3e-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="5bb3e-116">Name</span></span> | <span data-ttu-id="5bb3e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5bb3e-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb3e-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5bb3e-118">Element Type</span></span> <br/>   | <span data-ttu-id="5bb3e-119">Característica</span><span class="sxs-lookup"><span data-stu-id="5bb3e-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="5bb3e-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5bb3e-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5bb3e-121">Página</span><span class="sxs-lookup"><span data-stu-id="5bb3e-121">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="5bb3e-122">Notas</span><span class="sxs-lookup"><span data-stu-id="5bb3e-122">Notes</span></span> <br/>          | <span data-ttu-id="5bb3e-123">Las coordenadas son relativas a PageImageableSize, donde el origen de la marca de agua es relativo al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-123">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5bb3e-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="5bb3e-124">Structural Content</span></span>

<span data-ttu-id="5bb3e-125">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="5bb3e-125">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="5bb3e-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="5bb3e-126">Structure Variables</span></span>

<span data-ttu-id="5bb3e-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5bb3e-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="5bb3e-128">Name</span></span>                               | <span data-ttu-id="5bb3e-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5bb3e-129">Data type</span></span>         | <span data-ttu-id="5bb3e-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="5bb3e-130">Unit</span></span>                  | <span data-ttu-id="5bb3e-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="5bb3e-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5bb3e-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="5bb3e-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5bb3e-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5bb3e-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5bb3e-134">string</span><span class="sxs-lookup"><span data-stu-id="5bb3e-134">string</span></span><br/> | <span data-ttu-id="5bb3e-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="5bb3e-135">characters</span></span><br/> | <span data-ttu-id="5bb3e-136">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5bb3e-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5bb3e-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5bb3e-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5bb3e-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5bb3e-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5bb3e-140">string</span><span class="sxs-lookup"><span data-stu-id="5bb3e-140">string</span></span><br/> | <span data-ttu-id="5bb3e-141">N/D</span><span class="sxs-lookup"><span data-stu-id="5bb3e-141">n/a</span></span><br/>        | <span data-ttu-id="5bb3e-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5bb3e-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="5bb3e-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5bb3e-144">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5bb3e-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5bb3e-145">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="5bb3e-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5bb3e-146">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="5bb3e-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5bb3e-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5bb3e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bb3e-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5bb3e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




