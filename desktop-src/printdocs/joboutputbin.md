---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973433ac7f6e051d4656777696cc3a37cedd953b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999222"
---
# <a name="joboutputbin"></a><span data-ttu-id="0bc65-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="0bc65-104">JobOutputBin</span></span>

<span data-ttu-id="0bc65-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="0bc65-105">This topic is not current.</span></span> <span data-ttu-id="0bc65-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0bc65-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0bc65-107">Describe la ubicación de salida instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bc65-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="0bc65-108">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="0bc65-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="0bc65-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0bc65-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0bc65-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0bc65-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0bc65-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0bc65-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0bc65-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0bc65-112">Element Information</span></span>



| <span data-ttu-id="0bc65-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="0bc65-113">Name</span></span> | <span data-ttu-id="0bc65-114">Value</span><span class="sxs-lookup"><span data-stu-id="0bc65-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0bc65-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0bc65-115">Element Type</span></span> <br/>   | <span data-ttu-id="0bc65-116">Característica</span><span class="sxs-lookup"><span data-stu-id="0bc65-116">Feature</span></span><br/> |
| <span data-ttu-id="0bc65-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="0bc65-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0bc65-118">Trabajo</span><span class="sxs-lookup"><span data-stu-id="0bc65-118">Job</span></span><br/>     |
| <span data-ttu-id="0bc65-119">Notas</span><span class="sxs-lookup"><span data-stu-id="0bc65-119">Notes</span></span> <br/>          | <span data-ttu-id="0bc65-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0bc65-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0bc65-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0bc65-121">Structural Content</span></span>

<span data-ttu-id="0bc65-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="0bc65-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0bc65-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="0bc65-123">Structure Variables</span></span>

<span data-ttu-id="0bc65-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="0bc65-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0bc65-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="0bc65-125">Name</span></span>                                   | <span data-ttu-id="0bc65-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0bc65-126">Data type</span></span>          | <span data-ttu-id="0bc65-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="0bc65-127">Unit</span></span>                  | <span data-ttu-id="0bc65-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="0bc65-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0bc65-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="0bc65-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc65-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0bc65-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="0bc65-131">string</span><span class="sxs-lookup"><span data-stu-id="0bc65-131">string</span></span><br/>  | <span data-ttu-id="0bc65-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="0bc65-132">characters</span></span><br/> | <span data-ttu-id="0bc65-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0bc65-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0bc65-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0bc65-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0bc65-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="0bc65-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="0bc65-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0bc65-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="0bc65-137">string</span><span class="sxs-lookup"><span data-stu-id="0bc65-137">string</span></span><br/>  | <span data-ttu-id="0bc65-138">N/D</span><span class="sxs-lookup"><span data-stu-id="0bc65-138">n/a</span></span><br/>        | <span data-ttu-id="0bc65-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="0bc65-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0bc65-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="0bc65-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="0bc65-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="0bc65-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="0bc65-142">string</span><span class="sxs-lookup"><span data-stu-id="0bc65-142">string</span></span><br/>  | <span data-ttu-id="0bc65-143">N/D</span><span class="sxs-lookup"><span data-stu-id="0bc65-143">n/a</span></span><br/>        | <span data-ttu-id="0bc65-144">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="0bc65-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="0bc65-145">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="0bc65-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="0bc65-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="0bc65-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="0bc65-147">integer</span><span class="sxs-lookup"><span data-stu-id="0bc65-147">integer</span></span><br/> | <span data-ttu-id="0bc65-148">Hojas</span><span class="sxs-lookup"><span data-stu-id="0bc65-148">sheets</span></span><br/>     | <span data-ttu-id="0bc65-149">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bc65-149">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="0bc65-150">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="0bc65-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0bc65-151">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0bc65-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0bc65-152">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="0bc65-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0bc65-153">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="0bc65-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0bc65-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bc65-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc65-155">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0bc65-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




