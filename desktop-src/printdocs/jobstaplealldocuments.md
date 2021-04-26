---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9abf6184c3164e0e5a1492911e15794ea7e1d948
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993912"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="304c4-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="304c4-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="304c4-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="304c4-105">This topic is not current.</span></span> <span data-ttu-id="304c4-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="304c4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="304c4-107">Describe las características de estapling de la salida.</span><span class="sxs-lookup"><span data-stu-id="304c4-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="304c4-108">Todos los documentos del trabajo se apilen juntos.</span><span class="sxs-lookup"><span data-stu-id="304c4-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="304c4-109">Las palabras clave JobStapleAllDocuments y DocumentStaple son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="304c4-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="304c4-110">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="304c4-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="304c4-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="304c4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="304c4-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="304c4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="304c4-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="304c4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="304c4-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="304c4-114">Element Information</span></span>



| <span data-ttu-id="304c4-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="304c4-115">Name</span></span> | <span data-ttu-id="304c4-116">Value</span><span class="sxs-lookup"><span data-stu-id="304c4-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="304c4-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="304c4-117">Element Type</span></span> <br/>   | <span data-ttu-id="304c4-118">Característica</span><span class="sxs-lookup"><span data-stu-id="304c4-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="304c4-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="304c4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="304c4-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="304c4-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="304c4-121">Notas</span><span class="sxs-lookup"><span data-stu-id="304c4-121">Notes</span></span> <br/>          | <span data-ttu-id="304c4-122">Top, Bottom, Left y Right son relativos a PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="304c4-122">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="304c4-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="304c4-123">Structural Content</span></span>

<span data-ttu-id="304c4-124">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="304c4-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="304c4-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="304c4-125">Structure Variables</span></span>

<span data-ttu-id="304c4-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="304c4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="304c4-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="304c4-127">Name</span></span>                               | <span data-ttu-id="304c4-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="304c4-128">Data type</span></span>          | <span data-ttu-id="304c4-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="304c4-129">Unit</span></span>                       | <span data-ttu-id="304c4-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="304c4-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="304c4-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="304c4-131">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304c4-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="304c4-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="304c4-133">string</span><span class="sxs-lookup"><span data-stu-id="304c4-133">string</span></span><br/>  | <span data-ttu-id="304c4-134">Characters</span><span class="sxs-lookup"><span data-stu-id="304c4-134">Characters</span></span><br/>      | <span data-ttu-id="304c4-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="304c4-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="304c4-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="304c4-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="304c4-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="304c4-137">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="304c4-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="304c4-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="304c4-139">string</span><span class="sxs-lookup"><span data-stu-id="304c4-139">string</span></span><br/>  | <span data-ttu-id="304c4-140">N/D</span><span class="sxs-lookup"><span data-stu-id="304c4-140">n/a</span></span><br/>             | <span data-ttu-id="304c4-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="304c4-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="304c4-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="304c4-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="304c4-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="304c4-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="304c4-144">integer</span><span class="sxs-lookup"><span data-stu-id="304c4-144">integer</span></span><br/> | <span data-ttu-id="304c4-145">grados</span><span class="sxs-lookup"><span data-stu-id="304c4-145">degrees</span></span><br/>         | <span data-ttu-id="304c4-146">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="304c4-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="304c4-147">Especifica el ángulo de la grapa, en relación con el ancho de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="304c4-147">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="304c4-148">El ángulo de la grapa se mide en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="304c4-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="304c4-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="304c4-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="304c4-150">integer</span><span class="sxs-lookup"><span data-stu-id="304c4-150">integer</span></span><br/> | <span data-ttu-id="304c4-151">hojas de medios</span><span class="sxs-lookup"><span data-stu-id="304c4-151">sheets of media</span></span><br/> | <span data-ttu-id="304c4-152">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="304c4-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="304c4-153">Especifica el número de hojas admitidas por la opción de stapling para el elemento MediaType seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="304c4-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="304c4-154">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="304c4-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="304c4-155">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="304c4-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="304c4-156">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="304c4-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
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

## <a name="related-topics"></a><span data-ttu-id="304c4-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="304c4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="304c4-158">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="304c4-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




