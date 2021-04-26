---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338a72baecc62d22ac63ef50d8ce8967c7fd534a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997042"
---
# <a name="documentstaple"></a><span data-ttu-id="8ddf6-104">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="8ddf6-104">DocumentStaple</span></span>

<span data-ttu-id="8ddf6-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-105">This topic is not current.</span></span> <span data-ttu-id="8ddf6-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8ddf6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8ddf6-107">Describe las características de escalonamiento de la salida.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="8ddf6-108">Cada documento se grapa por separado.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-108">Each document is stapled separately.</span></span> <span data-ttu-id="8ddf6-109">Las palabras clave JobStapleAllDocuments y DocumentStaple son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="8ddf6-110">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="8ddf6-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8ddf6-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8ddf6-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="8ddf6-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8ddf6-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8ddf6-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8ddf6-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8ddf6-114">Element Information</span></span>



| <span data-ttu-id="8ddf6-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ddf6-115">Name</span></span> | <span data-ttu-id="8ddf6-116">Value</span><span class="sxs-lookup"><span data-stu-id="8ddf6-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8ddf6-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8ddf6-117">Element Type</span></span> <br/>   | <span data-ttu-id="8ddf6-118">Característica</span><span class="sxs-lookup"><span data-stu-id="8ddf6-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="8ddf6-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="8ddf6-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8ddf6-120">Documento</span><span class="sxs-lookup"><span data-stu-id="8ddf6-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="8ddf6-121">Notas</span><span class="sxs-lookup"><span data-stu-id="8ddf6-121">Notes</span></span> <br/>          | <span data-ttu-id="8ddf6-122">Top, Bottom, Left y Right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="8ddf6-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="8ddf6-123">Structural Content</span></span>

<span data-ttu-id="8ddf6-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="8ddf6-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="8ddf6-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="8ddf6-125">Structure Variables</span></span>

<span data-ttu-id="8ddf6-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8ddf6-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ddf6-127">Name</span></span>                               | <span data-ttu-id="8ddf6-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8ddf6-128">Data type</span></span>          | <span data-ttu-id="8ddf6-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="8ddf6-129">Unit</span></span>                       | <span data-ttu-id="8ddf6-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="8ddf6-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8ddf6-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="8ddf6-131">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ddf6-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8ddf6-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8ddf6-133">string</span><span class="sxs-lookup"><span data-stu-id="8ddf6-133">string</span></span><br/>  | <span data-ttu-id="8ddf6-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="8ddf6-134">characters</span></span><br/>      | <span data-ttu-id="8ddf6-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="8ddf6-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8ddf6-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8ddf6-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-137">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="8ddf6-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8ddf6-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8ddf6-139">string</span><span class="sxs-lookup"><span data-stu-id="8ddf6-139">string</span></span><br/>  | <span data-ttu-id="8ddf6-140">N/D</span><span class="sxs-lookup"><span data-stu-id="8ddf6-140">n/a</span></span><br/>             | <span data-ttu-id="8ddf6-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8ddf6-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="8ddf6-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="8ddf6-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="8ddf6-144">integer</span><span class="sxs-lookup"><span data-stu-id="8ddf6-144">integer</span></span><br/> | <span data-ttu-id="8ddf6-145">grados</span><span class="sxs-lookup"><span data-stu-id="8ddf6-145">degrees</span></span><br/>         | <span data-ttu-id="8ddf6-146">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="8ddf6-147">Especifica el ángulo de la grapa, con respecto a la dirección X de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-147">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="8ddf6-148">El ángulo de los ángulos se mide en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="8ddf6-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="8ddf6-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="8ddf6-150">integer</span><span class="sxs-lookup"><span data-stu-id="8ddf6-150">integer</span></span><br/> | <span data-ttu-id="8ddf6-151">hojas de medios</span><span class="sxs-lookup"><span data-stu-id="8ddf6-151">sheets of media</span></span><br/> | <span data-ttu-id="8ddf6-152">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="8ddf6-153">Especifica el número de hojas admitidas por la opción de stapling para el elemento MediaType seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="8ddf6-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8ddf6-154">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8ddf6-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8ddf6-155">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="8ddf6-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8ddf6-156">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="8ddf6-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None" />
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="8ddf6-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ddf6-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ddf6-158">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8ddf6-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




