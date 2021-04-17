---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41af04cc5657360fcc8d4b15812e9c2dd6b9fb06
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707645"
---
# <a name="pagescaling"></a><span data-ttu-id="e09bb-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="e09bb-104">PageScaling</span></span>

<span data-ttu-id="e09bb-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="e09bb-105">This topic is not current.</span></span> <span data-ttu-id="e09bb-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e09bb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e09bb-107">Describe las características de escalado de la salida.</span><span class="sxs-lookup"><span data-stu-id="e09bb-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="e09bb-108">Ciertas opciones de esta característica requieren que el consumidor pueda determinar las características de las "dimensiones de contenido de la aplicación".</span><span class="sxs-lookup"><span data-stu-id="e09bb-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="e09bb-109">En ausencia de la capacidad de determinar estas características, el consumidor debería tener como valor predeterminado la opción de identidad.</span><span class="sxs-lookup"><span data-stu-id="e09bb-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="e09bb-110">Estas características son:</span><span class="sxs-lookup"><span data-stu-id="e09bb-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09bb-111">Tamaño de los medios de aplicación</span><span class="sxs-lookup"><span data-stu-id="e09bb-111">Application Media Size</span></span>   | <span data-ttu-id="e09bb-112">Dimensiones del medio definido por el diseño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e09bb-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="e09bb-113">Es posible que el tamaño del medio de aplicación corresponda o no a un PageMediaSize admitido por el consumidor.</span><span class="sxs-lookup"><span data-stu-id="e09bb-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="e09bb-114">Tamaño del contenido de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e09bb-114">Application Content Size</span></span> | <span data-ttu-id="e09bb-115">Dimensiones del medio definido por el diseño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e09bb-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="e09bb-116">Es posible que el tamaño del medio de aplicación corresponda o no a un PageMediaSize admitido por el consumidor.</span><span class="sxs-lookup"><span data-stu-id="e09bb-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="e09bb-117">Tamaño de sangrado de aplicación</span><span class="sxs-lookup"><span data-stu-id="e09bb-117">Application Bleed Size</span></span>   | <span data-ttu-id="e09bb-118">El desplazamiento y la extensión del área de sangrado de la aplicación, un cuadro de desbordamiento usado por la aplicación para el registro y el diseño, en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e09bb-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="e09bb-119">El área de sangrado será mayor o igual que el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e09bb-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="e09bb-120">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e09bb-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e09bb-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e09bb-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e09bb-122">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="e09bb-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e09bb-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e09bb-123">Element Information</span></span>



| <span data-ttu-id="e09bb-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="e09bb-124">Name</span></span>                       |                                                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09bb-125">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e09bb-125">Element Type</span></span> <br/>   | <span data-ttu-id="e09bb-126">Característica</span><span class="sxs-lookup"><span data-stu-id="e09bb-126">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="e09bb-127">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e09bb-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e09bb-128">Página</span><span class="sxs-lookup"><span data-stu-id="e09bb-128">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="e09bb-129">Notas</span><span class="sxs-lookup"><span data-stu-id="e09bb-129">Notes</span></span> <br/>          | <span data-ttu-id="e09bb-130">Top, Bottom, left y right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="e09bb-130">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="e09bb-131">Las coordenadas son relativas a PageImageableSize, donde el origen de es relativo al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="e09bb-131">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e09bb-132">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e09bb-132">Structural Content</span></span>

<span data-ttu-id="e09bb-133">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e09bb-133">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="e09bb-134">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="e09bb-134">Structure Variables</span></span>

<span data-ttu-id="e09bb-135">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e09bb-135">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e09bb-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="e09bb-136">Name</span></span>                               | <span data-ttu-id="e09bb-137">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e09bb-137">Data type</span></span>         | <span data-ttu-id="e09bb-138">Unidad</span><span class="sxs-lookup"><span data-stu-id="e09bb-138">Unit</span></span>                  | <span data-ttu-id="e09bb-139">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="e09bb-139">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e09bb-140">Resumen</span><span class="sxs-lookup"><span data-stu-id="e09bb-140">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e09bb-141">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e09bb-141">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e09bb-142">string</span><span class="sxs-lookup"><span data-stu-id="e09bb-142">string</span></span><br/> | <span data-ttu-id="e09bb-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="e09bb-143">characters</span></span><br/> | <span data-ttu-id="e09bb-144">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e09bb-144">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e09bb-145">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e09bb-145">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e09bb-146">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="e09bb-146">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e09bb-147">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e09bb-147">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e09bb-148">string</span><span class="sxs-lookup"><span data-stu-id="e09bb-148">string</span></span><br/> | <span data-ttu-id="e09bb-149">N/D</span><span class="sxs-lookup"><span data-stu-id="e09bb-149">n/a</span></span><br/>        | <span data-ttu-id="e09bb-150">True, False.</span><span class="sxs-lookup"><span data-stu-id="e09bb-150">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e09bb-151">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="e09bb-151">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e09bb-152">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="e09bb-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e09bb-153">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e09bb-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e09bb-154">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="e09bb-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e09bb-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e09bb-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e09bb-156">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e09bb-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




