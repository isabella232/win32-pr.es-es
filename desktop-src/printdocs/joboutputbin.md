---
description: Obtenga información sobre el elemento JobOutputBin, que describe la ubicación de salida instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408858"
---
# <a name="joboutputbin"></a><span data-ttu-id="29495-103">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="29495-103">JobOutputBin</span></span>

<span data-ttu-id="29495-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="29495-104">This topic is not current.</span></span> <span data-ttu-id="29495-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="29495-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="29495-106">Describe la ubicación de salida instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29495-106">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="29495-107">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="29495-107">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="29495-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="29495-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="29495-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="29495-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="29495-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="29495-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="29495-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="29495-111">Element Information</span></span>



| <span data-ttu-id="29495-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="29495-112">Name</span></span> | <span data-ttu-id="29495-113">Valor</span><span class="sxs-lookup"><span data-stu-id="29495-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="29495-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="29495-114">Element Type</span></span> <br/>   | <span data-ttu-id="29495-115">Característica</span><span class="sxs-lookup"><span data-stu-id="29495-115">Feature</span></span><br/> |
| <span data-ttu-id="29495-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="29495-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="29495-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="29495-117">Job</span></span><br/>     |
| <span data-ttu-id="29495-118">Notas</span><span class="sxs-lookup"><span data-stu-id="29495-118">Notes</span></span> <br/>          | <span data-ttu-id="29495-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="29495-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="29495-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="29495-120">Structural Content</span></span>

<span data-ttu-id="29495-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="29495-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="29495-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="29495-122">Structure Variables</span></span>

<span data-ttu-id="29495-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="29495-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="29495-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="29495-124">Name</span></span>                                   | <span data-ttu-id="29495-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="29495-125">Data type</span></span>          | <span data-ttu-id="29495-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="29495-126">Unit</span></span>                  | <span data-ttu-id="29495-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="29495-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="29495-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="29495-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29495-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="29495-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="29495-130">string</span><span class="sxs-lookup"><span data-stu-id="29495-130">string</span></span><br/>  | <span data-ttu-id="29495-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="29495-131">characters</span></span><br/> | <span data-ttu-id="29495-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="29495-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="29495-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="29495-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="29495-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="29495-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="29495-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="29495-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="29495-136">string</span><span class="sxs-lookup"><span data-stu-id="29495-136">string</span></span><br/>  | <span data-ttu-id="29495-137">N/D</span><span class="sxs-lookup"><span data-stu-id="29495-137">n/a</span></span><br/>        | <span data-ttu-id="29495-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="29495-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="29495-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="29495-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="29495-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="29495-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="29495-141">string</span><span class="sxs-lookup"><span data-stu-id="29495-141">string</span></span><br/>  | <span data-ttu-id="29495-142">N/D</span><span class="sxs-lookup"><span data-stu-id="29495-142">n/a</span></span><br/>        | <span data-ttu-id="29495-143">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="29495-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="29495-144">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="29495-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="29495-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="29495-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="29495-146">integer</span><span class="sxs-lookup"><span data-stu-id="29495-146">integer</span></span><br/> | <span data-ttu-id="29495-147">Hojas</span><span class="sxs-lookup"><span data-stu-id="29495-147">sheets</span></span><br/>     | <span data-ttu-id="29495-148">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29495-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="29495-149">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="29495-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="29495-150">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="29495-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="29495-151">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="29495-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="29495-152">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="29495-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="29495-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29495-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29495-154">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="29495-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




