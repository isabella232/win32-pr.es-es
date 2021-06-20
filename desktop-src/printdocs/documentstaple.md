---
description: Obtenga información sobre el elemento JobStapleAllDocuments, que describe las características de estampación de la salida.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2cda02c452ebb053c71811fb2642cea7371b2f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409138"
---
# <a name="documentstaple"></a><span data-ttu-id="3d630-103">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="3d630-103">DocumentStaple</span></span>

<span data-ttu-id="3d630-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="3d630-104">This topic is not current.</span></span> <span data-ttu-id="3d630-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3d630-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3d630-106">Describe las características de estapling de la salida.</span><span class="sxs-lookup"><span data-stu-id="3d630-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="3d630-107">Cada documento se grapa por separado.</span><span class="sxs-lookup"><span data-stu-id="3d630-107">Each document is stapled separately.</span></span> <span data-ttu-id="3d630-108">Las palabras clave JobStapleAllDocuments y DocumentStaple son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="3d630-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="3d630-109">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="3d630-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="3d630-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3d630-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3d630-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3d630-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3d630-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3d630-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3d630-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3d630-113">Element Information</span></span>



| <span data-ttu-id="3d630-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d630-114">Name</span></span> | <span data-ttu-id="3d630-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3d630-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3d630-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3d630-116">Element Type</span></span> <br/>   | <span data-ttu-id="3d630-117">Característica</span><span class="sxs-lookup"><span data-stu-id="3d630-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="3d630-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="3d630-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3d630-119">Documento</span><span class="sxs-lookup"><span data-stu-id="3d630-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="3d630-120">Notas</span><span class="sxs-lookup"><span data-stu-id="3d630-120">Notes</span></span> <br/>          | <span data-ttu-id="3d630-121">Top, Bottom, Left y Right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="3d630-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="3d630-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3d630-122">Structural Content</span></span>

<span data-ttu-id="3d630-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="3d630-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3d630-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="3d630-124">Structure Variables</span></span>

<span data-ttu-id="3d630-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="3d630-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3d630-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d630-126">Name</span></span>                               | <span data-ttu-id="3d630-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3d630-127">Data type</span></span>          | <span data-ttu-id="3d630-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="3d630-128">Unit</span></span>                       | <span data-ttu-id="3d630-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="3d630-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3d630-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="3d630-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d630-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="3d630-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3d630-132">string</span><span class="sxs-lookup"><span data-stu-id="3d630-132">string</span></span><br/>  | <span data-ttu-id="3d630-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="3d630-133">characters</span></span><br/>      | <span data-ttu-id="3d630-134">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="3d630-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3d630-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3d630-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3d630-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="3d630-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="3d630-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3d630-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3d630-138">string</span><span class="sxs-lookup"><span data-stu-id="3d630-138">string</span></span><br/>  | <span data-ttu-id="3d630-139">N/D</span><span class="sxs-lookup"><span data-stu-id="3d630-139">n/a</span></span><br/>             | <span data-ttu-id="3d630-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="3d630-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3d630-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="3d630-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="3d630-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="3d630-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="3d630-143">integer</span><span class="sxs-lookup"><span data-stu-id="3d630-143">integer</span></span><br/> | <span data-ttu-id="3d630-144">grados</span><span class="sxs-lookup"><span data-stu-id="3d630-144">degrees</span></span><br/>         | <span data-ttu-id="3d630-145">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="3d630-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="3d630-146">Especifica el ángulo de la grapa, con respecto a la dirección X de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="3d630-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="3d630-147">El ángulo de los ángulos se mide en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="3d630-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="3d630-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="3d630-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="3d630-149">integer</span><span class="sxs-lookup"><span data-stu-id="3d630-149">integer</span></span><br/> | <span data-ttu-id="3d630-150">hojas de medios</span><span class="sxs-lookup"><span data-stu-id="3d630-150">sheets of media</span></span><br/> | <span data-ttu-id="3d630-151">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="3d630-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="3d630-152">Especifica el número de hojas admitidas por la opción de stapling para el MediaType seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3d630-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3d630-153">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3d630-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3d630-154">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="3d630-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3d630-155">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="3d630-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3d630-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d630-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d630-157">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3d630-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




