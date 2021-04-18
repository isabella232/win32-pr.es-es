---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d0e0e47aa89a3cb6380a78dd49312d17f88ab8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717449"
---
# <a name="pagewatermark"></a><span data-ttu-id="12899-104">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="12899-104">PageWatermark</span></span>

<span data-ttu-id="12899-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="12899-105">This topic is not current.</span></span> <span data-ttu-id="12899-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="12899-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="12899-107">Describe el valor de marca de agua de la salida y las características de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="12899-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="12899-108">Las marcas de agua se aplican a la página lógica, no a la página física.</span><span class="sxs-lookup"><span data-stu-id="12899-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="12899-109">Por ejemplo, si DocumentDuplex está habilitado, aparecerá una marca de agua en cada página de NUp de cada hoja.</span><span class="sxs-lookup"><span data-stu-id="12899-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="12899-110">Si DocumentDuplex, PagesPerSheet = 2, cada hoja tendrá 2 marcas de agua.</span><span class="sxs-lookup"><span data-stu-id="12899-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="12899-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="12899-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="12899-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="12899-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="12899-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="12899-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="12899-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="12899-114">Element Information</span></span>



| <span data-ttu-id="12899-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="12899-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12899-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="12899-116">Element Type</span></span> <br/>   | <span data-ttu-id="12899-117">Característica</span><span class="sxs-lookup"><span data-stu-id="12899-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="12899-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="12899-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="12899-119">Página</span><span class="sxs-lookup"><span data-stu-id="12899-119">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="12899-120">Notas</span><span class="sxs-lookup"><span data-stu-id="12899-120">Notes</span></span> <br/>          | <span data-ttu-id="12899-121">Las coordenadas son relativas a PageImageableSize, donde el origen de la marca de agua es relativo al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="12899-121">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="12899-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="12899-122">Structural Content</span></span>

<span data-ttu-id="12899-123">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="12899-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="12899-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="12899-124">Structure Variables</span></span>

<span data-ttu-id="12899-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="12899-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="12899-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="12899-126">Name</span></span>                               | <span data-ttu-id="12899-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="12899-127">Data type</span></span>         | <span data-ttu-id="12899-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="12899-128">Unit</span></span>                  | <span data-ttu-id="12899-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="12899-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="12899-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="12899-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="12899-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="12899-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="12899-132">string</span><span class="sxs-lookup"><span data-stu-id="12899-132">string</span></span><br/> | <span data-ttu-id="12899-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="12899-133">characters</span></span><br/> | <span data-ttu-id="12899-134">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="12899-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="12899-135">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="12899-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="12899-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="12899-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="12899-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="12899-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="12899-138">string</span><span class="sxs-lookup"><span data-stu-id="12899-138">string</span></span><br/> | <span data-ttu-id="12899-139">N/D</span><span class="sxs-lookup"><span data-stu-id="12899-139">n/a</span></span><br/>        | <span data-ttu-id="12899-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="12899-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="12899-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="12899-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="12899-142">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="12899-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="12899-143">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="12899-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="12899-144">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="12899-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="12899-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12899-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12899-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="12899-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




