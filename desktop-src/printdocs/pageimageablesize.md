---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996112"
---
# <a name="pageimageablesize"></a><span data-ttu-id="d9bf0-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="d9bf0-104">PageImageableSize</span></span>

<span data-ttu-id="d9bf0-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-105">This topic is not current.</span></span> <span data-ttu-id="d9bf0-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d9bf0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d9bf0-107">Describe el lienzo con imágenes para el diseño y la representación.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="d9bf0-108">Esto se notifica en función de PageMediaSize y PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="d9bf0-109">Los diagramas siguientes ilustran el uso de variables PageImageableSize basadas en PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![un diagrama que muestra las medidas de página](images/local-1641910626-image.png)

-   [<span data-ttu-id="d9bf0-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d9bf0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d9bf0-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d9bf0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d9bf0-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d9bf0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d9bf0-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d9bf0-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="d9bf0-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9bf0-115">Name</span></span> | <span data-ttu-id="d9bf0-116">Value</span><span class="sxs-lookup"><span data-stu-id="d9bf0-116">Value</span></span> |
| <span data-ttu-id="d9bf0-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d9bf0-117">Element Type</span></span><br/>    | <span data-ttu-id="d9bf0-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9bf0-118">Property</span></span><br/> |
| <span data-ttu-id="d9bf0-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d9bf0-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d9bf0-120">Página</span><span class="sxs-lookup"><span data-stu-id="d9bf0-120">Page</span></span><br/>     |
| <span data-ttu-id="d9bf0-121">Notas</span><span class="sxs-lookup"><span data-stu-id="d9bf0-121">Notes</span></span> <br/>          | <span data-ttu-id="d9bf0-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d9bf0-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d9bf0-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d9bf0-123">Structural Content</span></span>

<span data-ttu-id="d9bf0-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d9bf0-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d9bf0-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="d9bf0-125">Structure Variables</span></span>

<span data-ttu-id="d9bf0-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d9bf0-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9bf0-127">Name</span></span>                                    | <span data-ttu-id="d9bf0-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d9bf0-128">Data type</span></span>          | <span data-ttu-id="d9bf0-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="d9bf0-129">Unit</span></span>               | <span data-ttu-id="d9bf0-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="d9bf0-130">Supported values</span></span>                       | <span data-ttu-id="d9bf0-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="d9bf0-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bf0-132">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d9bf0-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="d9bf0-133">integer</span><span class="sxs-lookup"><span data-stu-id="d9bf0-133">integer</span></span><br/> | <span data-ttu-id="d9bf0-134">Micras</span><span class="sxs-lookup"><span data-stu-id="d9bf0-134">microns</span></span><br/> | <span data-ttu-id="d9bf0-135">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="d9bf0-136">Especifica la dimensión horizontal del tamaño del medio de aplicación con respecto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="d9bf0-137">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d9bf0-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="d9bf0-138">integer</span><span class="sxs-lookup"><span data-stu-id="d9bf0-138">integer</span></span><br/> | <span data-ttu-id="d9bf0-139">Micras</span><span class="sxs-lookup"><span data-stu-id="d9bf0-139">microns</span></span><br/> | <span data-ttu-id="d9bf0-140">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="d9bf0-141">Especifica la dimensión vertical del tamaño del medio de la aplicación con respecto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="d9bf0-142">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d9bf0-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="d9bf0-143">integer</span><span class="sxs-lookup"><span data-stu-id="d9bf0-143">integer</span></span><br/> | <span data-ttu-id="d9bf0-144">Micras</span><span class="sxs-lookup"><span data-stu-id="d9bf0-144">microns</span></span><br/> | <span data-ttu-id="d9bf0-145">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="d9bf0-146">Especifica el origen horizontal del área en la que se pueden crear imágenes en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="d9bf0-147">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d9bf0-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="d9bf0-148">integer</span><span class="sxs-lookup"><span data-stu-id="d9bf0-148">integer</span></span><br/> | <span data-ttu-id="d9bf0-149">Micras</span><span class="sxs-lookup"><span data-stu-id="d9bf0-149">microns</span></span><br/> | <span data-ttu-id="d9bf0-150">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="d9bf0-151">Especifica el origen vertical del área en la que se pueden crear imágenes en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="d9bf0-152">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d9bf0-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="d9bf0-153">integer</span><span class="sxs-lookup"><span data-stu-id="d9bf0-153">integer</span></span><br/> | <span data-ttu-id="d9bf0-154">Micras</span><span class="sxs-lookup"><span data-stu-id="d9bf0-154">microns</span></span><br/> | <span data-ttu-id="d9bf0-155">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="d9bf0-156">Especifica la distancia horizontal entre el origen y el límite del tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="d9bf0-157">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d9bf0-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="d9bf0-158">integer</span><span class="sxs-lookup"><span data-stu-id="d9bf0-158">integer</span></span><br/> | <span data-ttu-id="d9bf0-159">Micras</span><span class="sxs-lookup"><span data-stu-id="d9bf0-159">microns</span></span><br/> | <span data-ttu-id="d9bf0-160">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="d9bf0-161">Especifica la distancia vertical entre el origen y el límite del tamaño del medio de la aplicación de lienzo.</span><span class="sxs-lookup"><span data-stu-id="d9bf0-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d9bf0-162">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d9bf0-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d9bf0-163">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="d9bf0-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d9bf0-164">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="d9bf0-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="d9bf0-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9bf0-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9bf0-166">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d9bf0-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




