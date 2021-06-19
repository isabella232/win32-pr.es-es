---
description: Obtenga información sobre el elemento configurable por el usuario PageImageableSize. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395310"
---
# <a name="pageimageablesize"></a><span data-ttu-id="56e0f-105">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="56e0f-105">PageImageableSize</span></span>

<span data-ttu-id="56e0f-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="56e0f-106">This topic is not current.</span></span> <span data-ttu-id="56e0f-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56e0f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56e0f-108">Describe el lienzo con imágenes para el diseño y la representación.</span><span class="sxs-lookup"><span data-stu-id="56e0f-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="56e0f-109">Esto se notifica en función de PageMediaSize y PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="56e0f-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="56e0f-110">En los diagramas siguientes se muestra el uso de variables PageImageableSize basadas en PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="56e0f-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![un diagrama que muestra las medidas de página](images/local-1641910626-image.png)

-   [<span data-ttu-id="56e0f-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="56e0f-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56e0f-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="56e0f-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="56e0f-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="56e0f-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="56e0f-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="56e0f-115">Element Information</span></span>

| <span data-ttu-id="56e0f-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="56e0f-116">Name</span></span>                 | <span data-ttu-id="56e0f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="56e0f-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="56e0f-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="56e0f-118">Element Type</span></span><br/>    | <span data-ttu-id="56e0f-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56e0f-119">Property</span></span><br/> |
| <span data-ttu-id="56e0f-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="56e0f-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56e0f-121">Página</span><span class="sxs-lookup"><span data-stu-id="56e0f-121">Page</span></span><br/>     |
| <span data-ttu-id="56e0f-122">Notas</span><span class="sxs-lookup"><span data-stu-id="56e0f-122">Notes</span></span> <br/>          | <span data-ttu-id="56e0f-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="56e0f-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="56e0f-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="56e0f-124">Structural Content</span></span>

<span data-ttu-id="56e0f-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="56e0f-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="56e0f-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="56e0f-126">Structure Variables</span></span>

<span data-ttu-id="56e0f-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="56e0f-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56e0f-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="56e0f-128">Name</span></span>                                    | <span data-ttu-id="56e0f-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="56e0f-129">Data type</span></span>          | <span data-ttu-id="56e0f-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="56e0f-130">Unit</span></span>               | <span data-ttu-id="56e0f-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="56e0f-131">Supported values</span></span>                       | <span data-ttu-id="56e0f-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="56e0f-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e0f-133">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="56e0f-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="56e0f-134">integer</span><span class="sxs-lookup"><span data-stu-id="56e0f-134">integer</span></span><br/> | <span data-ttu-id="56e0f-135">Micras</span><span class="sxs-lookup"><span data-stu-id="56e0f-135">microns</span></span><br/> | <span data-ttu-id="56e0f-136">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0f-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="56e0f-137">Especifica la dimensión horizontal del tamaño del medio de la aplicación con respecto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="56e0f-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="56e0f-138">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="56e0f-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="56e0f-139">integer</span><span class="sxs-lookup"><span data-stu-id="56e0f-139">integer</span></span><br/> | <span data-ttu-id="56e0f-140">Micras</span><span class="sxs-lookup"><span data-stu-id="56e0f-140">microns</span></span><br/> | <span data-ttu-id="56e0f-141">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0f-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="56e0f-142">Especifica la dimensión vertical del tamaño del medio de la aplicación con respecto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="56e0f-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="56e0f-143">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="56e0f-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="56e0f-144">integer</span><span class="sxs-lookup"><span data-stu-id="56e0f-144">integer</span></span><br/> | <span data-ttu-id="56e0f-145">Micras</span><span class="sxs-lookup"><span data-stu-id="56e0f-145">microns</span></span><br/> | <span data-ttu-id="56e0f-146">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0f-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="56e0f-147">Especifica el origen horizontal del área en la que se pueden crear imágenes en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56e0f-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="56e0f-148">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="56e0f-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="56e0f-149">integer</span><span class="sxs-lookup"><span data-stu-id="56e0f-149">integer</span></span><br/> | <span data-ttu-id="56e0f-150">Micras</span><span class="sxs-lookup"><span data-stu-id="56e0f-150">microns</span></span><br/> | <span data-ttu-id="56e0f-151">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0f-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="56e0f-152">Especifica el origen vertical del área en la que se pueden crear imágenes en relación con el tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56e0f-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="56e0f-153">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="56e0f-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="56e0f-154">integer</span><span class="sxs-lookup"><span data-stu-id="56e0f-154">integer</span></span><br/> | <span data-ttu-id="56e0f-155">Micras</span><span class="sxs-lookup"><span data-stu-id="56e0f-155">microns</span></span><br/> | <span data-ttu-id="56e0f-156">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0f-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="56e0f-157">Especifica la distancia horizontal entre el origen y el límite del tamaño del medio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56e0f-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="56e0f-158">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="56e0f-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="56e0f-159">integer</span><span class="sxs-lookup"><span data-stu-id="56e0f-159">integer</span></span><br/> | <span data-ttu-id="56e0f-160">Micras</span><span class="sxs-lookup"><span data-stu-id="56e0f-160">microns</span></span><br/> | <span data-ttu-id="56e0f-161">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0f-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="56e0f-162">Especifica la distancia vertical entre el origen y el límite del tamaño del medio de la aplicación de lienzo.</span><span class="sxs-lookup"><span data-stu-id="56e0f-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="56e0f-163">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="56e0f-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="56e0f-164">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="56e0f-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="56e0f-165">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="56e0f-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="56e0f-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56e0f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56e0f-167">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="56e0f-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




