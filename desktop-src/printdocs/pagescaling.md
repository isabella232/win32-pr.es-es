---
description: Obtenga información sobre el elemento PageScaling. Este elemento describe las características de escalado de la salida.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795332f38da331a9f16b614154bf0a9270e613de
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119040"
---
# <a name="pagescaling"></a><span data-ttu-id="7711f-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="7711f-104">PageScaling</span></span>

<span data-ttu-id="7711f-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="7711f-105">This topic is not current.</span></span> <span data-ttu-id="7711f-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7711f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7711f-107">Describe las características de escalado de la salida.</span><span class="sxs-lookup"><span data-stu-id="7711f-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="7711f-108">Algunas opciones de esta característica requieren que el consumidor pueda determinar las características de las "dimensiones de contenido de la aplicación".</span><span class="sxs-lookup"><span data-stu-id="7711f-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="7711f-109">En ausencia de la capacidad de determinar estas características, el consumidor debe establecer de forma predeterminada la opción de identidad.</span><span class="sxs-lookup"><span data-stu-id="7711f-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="7711f-110">Estas características son:</span><span class="sxs-lookup"><span data-stu-id="7711f-110">These characteristics are:</span></span>



| <span data-ttu-id="7711f-111">Característica de escalado</span><span class="sxs-lookup"><span data-stu-id="7711f-111">Scaling characteristic</span></span>                         | <span data-ttu-id="7711f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7711f-112">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7711f-113">Tamaño del medio de aplicación</span><span class="sxs-lookup"><span data-stu-id="7711f-113">Application Media Size</span></span>   | <span data-ttu-id="7711f-114">Dimensiones del medio definido por el diseño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7711f-114">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="7711f-115">El tamaño del medio de aplicación puede o no corresponder a pageMediaSize compatible con el consumidor.</span><span class="sxs-lookup"><span data-stu-id="7711f-115">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="7711f-116">Tamaño del contenido de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7711f-116">Application Content Size</span></span> | <span data-ttu-id="7711f-117">Dimensiones del medio definido por el diseño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7711f-117">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="7711f-118">El tamaño del medio de aplicación puede o no corresponder a pageMediaSize compatible con el consumidor.</span><span class="sxs-lookup"><span data-stu-id="7711f-118">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="7711f-119">Tamaño de la sangría de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7711f-119">Application Bleed Size</span></span>   | <span data-ttu-id="7711f-120">Desplazamiento y extensión del área de sangría de la aplicación, un cuadro de desbordamiento utilizado por la aplicación para el registro y el diseño, en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7711f-120">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="7711f-121">El área de purga será mayor o igual que el tamaño del medio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7711f-121">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="7711f-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7711f-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7711f-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="7711f-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7711f-124">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7711f-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7711f-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7711f-125">Element Information</span></span>



| <span data-ttu-id="7711f-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="7711f-126">Name</span></span> | <span data-ttu-id="7711f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7711f-127">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7711f-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7711f-128">Element Type</span></span> <br/>   | <span data-ttu-id="7711f-129">Característica</span><span class="sxs-lookup"><span data-stu-id="7711f-129">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="7711f-130">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7711f-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7711f-131">Página</span><span class="sxs-lookup"><span data-stu-id="7711f-131">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="7711f-132">Notas</span><span class="sxs-lookup"><span data-stu-id="7711f-132">Notes</span></span> <br/>          | <span data-ttu-id="7711f-133">Top, Bottom, Left y Right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="7711f-133">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="7711f-134">Las coordenadas son relativas a PageImageableSize, donde el origen de es relativo al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="7711f-134">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7711f-135">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="7711f-135">Structural Content</span></span>

<span data-ttu-id="7711f-136">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="7711f-136">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7711f-137">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="7711f-137">Structure Variables</span></span>

<span data-ttu-id="7711f-138">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7711f-138">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7711f-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="7711f-139">Name</span></span>                               | <span data-ttu-id="7711f-140">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7711f-140">Data type</span></span>         | <span data-ttu-id="7711f-141">Unidad</span><span class="sxs-lookup"><span data-stu-id="7711f-141">Unit</span></span>                  | <span data-ttu-id="7711f-142">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="7711f-142">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7711f-143">Resumen</span><span class="sxs-lookup"><span data-stu-id="7711f-143">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7711f-144">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7711f-144">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7711f-145">string</span><span class="sxs-lookup"><span data-stu-id="7711f-145">string</span></span><br/> | <span data-ttu-id="7711f-146">caracteres</span><span class="sxs-lookup"><span data-stu-id="7711f-146">characters</span></span><br/> | <span data-ttu-id="7711f-147">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7711f-147">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7711f-148">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7711f-148">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7711f-149">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="7711f-149">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7711f-150">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7711f-150">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7711f-151">string</span><span class="sxs-lookup"><span data-stu-id="7711f-151">string</span></span><br/> | <span data-ttu-id="7711f-152">N/D</span><span class="sxs-lookup"><span data-stu-id="7711f-152">n/a</span></span><br/>        | <span data-ttu-id="7711f-153">True, False.</span><span class="sxs-lookup"><span data-stu-id="7711f-153">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7711f-154">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="7711f-154">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7711f-155">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7711f-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7711f-156">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="7711f-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7711f-157">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="7711f-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7711f-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7711f-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7711f-159">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7711f-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




