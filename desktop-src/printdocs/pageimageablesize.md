---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104560245"
---
# <a name="pageimageablesize"></a><span data-ttu-id="31430-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="31430-104">PageImageableSize</span></span>

<span data-ttu-id="31430-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="31430-105">This topic is not current.</span></span> <span data-ttu-id="31430-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="31430-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="31430-107">Describe el lienzo con imagen para el diseño y la representación.</span><span class="sxs-lookup"><span data-stu-id="31430-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="31430-108">Se inscribirá en función de PageMediaSize y PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="31430-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="31430-109">En los diagramas siguientes se muestra el uso de variables de PageImageableSize basado en PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="31430-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagrama que muestra las medidas de página](images/local-1641910626-image.png)

-   [<span data-ttu-id="31430-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="31430-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="31430-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="31430-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="31430-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="31430-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="31430-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="31430-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="31430-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="31430-115">Name</span></span>                       |                     |
| <span data-ttu-id="31430-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="31430-116">Element Type</span></span><br/>    | <span data-ttu-id="31430-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31430-117">Property</span></span><br/> |
| <span data-ttu-id="31430-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="31430-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="31430-119">Página</span><span class="sxs-lookup"><span data-stu-id="31430-119">Page</span></span><br/>     |
| <span data-ttu-id="31430-120">Notas</span><span class="sxs-lookup"><span data-stu-id="31430-120">Notes</span></span> <br/>          | <span data-ttu-id="31430-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="31430-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="31430-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="31430-122">Structural Content</span></span>

<span data-ttu-id="31430-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="31430-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="31430-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="31430-124">Structure Variables</span></span>

<span data-ttu-id="31430-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="31430-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="31430-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="31430-126">Name</span></span>                                    | <span data-ttu-id="31430-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="31430-127">Data type</span></span>          | <span data-ttu-id="31430-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="31430-128">Unit</span></span>               | <span data-ttu-id="31430-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="31430-129">Supported values</span></span>                       | <span data-ttu-id="31430-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="31430-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31430-131">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="31430-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="31430-132">integer</span><span class="sxs-lookup"><span data-stu-id="31430-132">integer</span></span><br/> | <span data-ttu-id="31430-133">microns</span><span class="sxs-lookup"><span data-stu-id="31430-133">microns</span></span><br/> | <span data-ttu-id="31430-134">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="31430-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="31430-135">Especifica la dimensión horizontal del tamaño del medio de aplicación en relación con el PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="31430-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="31430-136">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="31430-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="31430-137">integer</span><span class="sxs-lookup"><span data-stu-id="31430-137">integer</span></span><br/> | <span data-ttu-id="31430-138">microns</span><span class="sxs-lookup"><span data-stu-id="31430-138">microns</span></span><br/> | <span data-ttu-id="31430-139">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="31430-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="31430-140">Especifica la dimensión vertical del tamaño del medio de aplicación en relación con el PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="31430-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="31430-141">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="31430-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="31430-142">integer</span><span class="sxs-lookup"><span data-stu-id="31430-142">integer</span></span><br/> | <span data-ttu-id="31430-143">microns</span><span class="sxs-lookup"><span data-stu-id="31430-143">microns</span></span><br/> | <span data-ttu-id="31430-144">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="31430-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="31430-145">Especifica el origen horizontal del área de impresión en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31430-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="31430-146">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="31430-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="31430-147">integer</span><span class="sxs-lookup"><span data-stu-id="31430-147">integer</span></span><br/> | <span data-ttu-id="31430-148">microns</span><span class="sxs-lookup"><span data-stu-id="31430-148">microns</span></span><br/> | <span data-ttu-id="31430-149">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="31430-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="31430-150">Especifica el origen vertical del área de impresión en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31430-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="31430-151">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="31430-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="31430-152">integer</span><span class="sxs-lookup"><span data-stu-id="31430-152">integer</span></span><br/> | <span data-ttu-id="31430-153">microns</span><span class="sxs-lookup"><span data-stu-id="31430-153">microns</span></span><br/> | <span data-ttu-id="31430-154">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="31430-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="31430-155">Especifica la distancia horizontal entre el origen y el límite de límite del tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31430-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="31430-156">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="31430-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="31430-157">integer</span><span class="sxs-lookup"><span data-stu-id="31430-157">integer</span></span><br/> | <span data-ttu-id="31430-158">microns</span><span class="sxs-lookup"><span data-stu-id="31430-158">microns</span></span><br/> | <span data-ttu-id="31430-159">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="31430-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="31430-160">Especifica la distancia vertical entre el origen y el límite de límite del tamaño del medio de la aplicación Canvas.</span><span class="sxs-lookup"><span data-stu-id="31430-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="31430-161">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="31430-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="31430-162">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="31430-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="31430-163">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="31430-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="31430-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31430-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31430-165">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="31430-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




