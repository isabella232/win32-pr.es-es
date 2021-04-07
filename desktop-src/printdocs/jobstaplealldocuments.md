---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3576611dcdc746342b8ed1b2c3d7ebf8fb779
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104003481"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="c55f6-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="c55f6-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="c55f6-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="c55f6-105">This topic is not current.</span></span> <span data-ttu-id="c55f6-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c55f6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c55f6-107">Describe las características de grapado de la salida.</span><span class="sxs-lookup"><span data-stu-id="c55f6-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="c55f6-108">Todos los documentos del trabajo se grapan juntos.</span><span class="sxs-lookup"><span data-stu-id="c55f6-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="c55f6-109">Las palabras clave JobStapleAllDocuments y DocumentStaple se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="c55f6-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="c55f6-110">Es el controlador el que determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="c55f6-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="c55f6-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c55f6-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c55f6-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c55f6-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c55f6-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c55f6-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c55f6-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c55f6-114">Element Information</span></span>



| <span data-ttu-id="c55f6-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="c55f6-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c55f6-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c55f6-116">Element Type</span></span> <br/>   | <span data-ttu-id="c55f6-117">Característica</span><span class="sxs-lookup"><span data-stu-id="c55f6-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="c55f6-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="c55f6-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c55f6-119">Trabajo</span><span class="sxs-lookup"><span data-stu-id="c55f6-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="c55f6-120">Notas</span><span class="sxs-lookup"><span data-stu-id="c55f6-120">Notes</span></span> <br/>          | <span data-ttu-id="c55f6-121">Top, Bottom, left y right son relativos a PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="c55f6-121">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c55f6-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c55f6-122">Structural Content</span></span>

<span data-ttu-id="c55f6-123">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="c55f6-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c55f6-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="c55f6-124">Structure Variables</span></span>

<span data-ttu-id="c55f6-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="c55f6-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c55f6-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="c55f6-126">Name</span></span>                               | <span data-ttu-id="c55f6-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c55f6-127">Data type</span></span>          | <span data-ttu-id="c55f6-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="c55f6-128">Unit</span></span>                       | <span data-ttu-id="c55f6-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="c55f6-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c55f6-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="c55f6-130">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c55f6-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c55f6-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c55f6-132">string</span><span class="sxs-lookup"><span data-stu-id="c55f6-132">string</span></span><br/>  | <span data-ttu-id="c55f6-133">Characters</span><span class="sxs-lookup"><span data-stu-id="c55f6-133">Characters</span></span><br/>      | <span data-ttu-id="c55f6-134">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c55f6-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c55f6-135">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c55f6-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c55f6-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="c55f6-136">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="c55f6-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c55f6-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c55f6-138">string</span><span class="sxs-lookup"><span data-stu-id="c55f6-138">string</span></span><br/>  | <span data-ttu-id="c55f6-139">N/D</span><span class="sxs-lookup"><span data-stu-id="c55f6-139">n/a</span></span><br/>             | <span data-ttu-id="c55f6-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="c55f6-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c55f6-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="c55f6-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="c55f6-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="c55f6-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="c55f6-143">integer</span><span class="sxs-lookup"><span data-stu-id="c55f6-143">integer</span></span><br/> | <span data-ttu-id="c55f6-144">grados</span><span class="sxs-lookup"><span data-stu-id="c55f6-144">degrees</span></span><br/>         | <span data-ttu-id="c55f6-145">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="c55f6-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="c55f6-146">Especifica el ángulo de grapado, en relación con el ancho del PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="c55f6-146">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="c55f6-147">El ángulo de grapa se mide en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="c55f6-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="c55f6-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="c55f6-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="c55f6-149">integer</span><span class="sxs-lookup"><span data-stu-id="c55f6-149">integer</span></span><br/> | <span data-ttu-id="c55f6-150">hojas de medios</span><span class="sxs-lookup"><span data-stu-id="c55f6-150">sheets of media</span></span><br/> | <span data-ttu-id="c55f6-151">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="c55f6-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="c55f6-152">Especifica el número de hojas admitidas por la opción grapado para el valor de MediaType seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="c55f6-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c55f6-153">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c55f6-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c55f6-154">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c55f6-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c55f6-155">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="c55f6-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c55f6-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c55f6-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c55f6-157">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c55f6-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




