---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43fcf4aaf389769625e2289a438d7d5c2be0b83
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707631"
---
# <a name="joboutputbin"></a><span data-ttu-id="74b81-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="74b81-104">JobOutputBin</span></span>

<span data-ttu-id="74b81-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="74b81-105">This topic is not current.</span></span> <span data-ttu-id="74b81-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74b81-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74b81-107">Describe la bandeja de salida instalada en un dispositivo o la lista completa de ubicaciones compatibles para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74b81-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="74b81-108">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin se excluyen mutuamente solo se debe especificar una en un documento de funcionalidades de impresión o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="74b81-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="74b81-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="74b81-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="74b81-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="74b81-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="74b81-111">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="74b81-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="74b81-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="74b81-112">Element Information</span></span>



| <span data-ttu-id="74b81-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="74b81-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="74b81-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="74b81-114">Element Type</span></span> <br/>   | <span data-ttu-id="74b81-115">Característica</span><span class="sxs-lookup"><span data-stu-id="74b81-115">Feature</span></span><br/> |
| <span data-ttu-id="74b81-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="74b81-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="74b81-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="74b81-117">Job</span></span><br/>     |
| <span data-ttu-id="74b81-118">Notas</span><span class="sxs-lookup"><span data-stu-id="74b81-118">Notes</span></span> <br/>          | <span data-ttu-id="74b81-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="74b81-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="74b81-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="74b81-120">Structural Content</span></span>

<span data-ttu-id="74b81-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="74b81-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="74b81-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="74b81-122">Structure Variables</span></span>

<span data-ttu-id="74b81-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="74b81-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="74b81-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="74b81-124">Name</span></span>                                   | <span data-ttu-id="74b81-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="74b81-125">Data type</span></span>          | <span data-ttu-id="74b81-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="74b81-126">Unit</span></span>                  | <span data-ttu-id="74b81-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="74b81-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="74b81-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="74b81-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74b81-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="74b81-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="74b81-130">string</span><span class="sxs-lookup"><span data-stu-id="74b81-130">string</span></span><br/>  | <span data-ttu-id="74b81-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="74b81-131">characters</span></span><br/> | <span data-ttu-id="74b81-132">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="74b81-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="74b81-133">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="74b81-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="74b81-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="74b81-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="74b81-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="74b81-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="74b81-136">string</span><span class="sxs-lookup"><span data-stu-id="74b81-136">string</span></span><br/>  | <span data-ttu-id="74b81-137">N/D</span><span class="sxs-lookup"><span data-stu-id="74b81-137">n/a</span></span><br/>        | <span data-ttu-id="74b81-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="74b81-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="74b81-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="74b81-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="74b81-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="74b81-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="74b81-141">string</span><span class="sxs-lookup"><span data-stu-id="74b81-141">string</span></span><br/>  | <span data-ttu-id="74b81-142">N/D</span><span class="sxs-lookup"><span data-stu-id="74b81-142">n/a</span></span><br/>        | <span data-ttu-id="74b81-143">Buzón, clasificador, apilador, dispositivo de acabado, ninguno.</span><span class="sxs-lookup"><span data-stu-id="74b81-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="74b81-144">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="74b81-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="74b81-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="74b81-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="74b81-146">integer</span><span class="sxs-lookup"><span data-stu-id="74b81-146">integer</span></span><br/> | <span data-ttu-id="74b81-147">Sheet</span><span class="sxs-lookup"><span data-stu-id="74b81-147">sheets</span></span><br/>     | <span data-ttu-id="74b81-148">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74b81-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="74b81-149">Especifica la capacidad de los medios en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="74b81-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="74b81-150">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="74b81-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="74b81-151">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="74b81-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="74b81-152">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="74b81-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="74b81-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74b81-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b81-154">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="74b81-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




