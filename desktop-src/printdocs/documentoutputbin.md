---
description: Obtenga información sobre DocumentOutputBin, que describe la lista completa de ubicaciones admitidas para el dispositivo y permite la especificación de la ubicación de salida por documento.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409248"
---
# <a name="documentoutputbin"></a><span data-ttu-id="9b5e4-103">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="9b5e4-103">DocumentOutputBin</span></span>

<span data-ttu-id="9b5e4-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-104">This topic is not current.</span></span> <span data-ttu-id="9b5e4-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b5e4-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b5e4-106">Describe la lista completa de ubicaciones admitidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="9b5e4-107">Permite la especificación de la ubicación de salida por documento.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="9b5e4-108">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9b5e4-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9b5e4-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="9b5e4-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9b5e4-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="9b5e4-111">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="9b5e4-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9b5e4-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9b5e4-112">Element Information</span></span>



| <span data-ttu-id="9b5e4-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b5e4-113">Name</span></span> | <span data-ttu-id="9b5e4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9b5e4-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="9b5e4-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9b5e4-115">Element Type</span></span> <br/>   | <span data-ttu-id="9b5e4-116">Característica</span><span class="sxs-lookup"><span data-stu-id="9b5e4-116">Feature</span></span><br/>  |
| <span data-ttu-id="9b5e4-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9b5e4-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9b5e4-118">Documento</span><span class="sxs-lookup"><span data-stu-id="9b5e4-118">Document</span></span><br/> |
| <span data-ttu-id="9b5e4-119">Notas</span><span class="sxs-lookup"><span data-stu-id="9b5e4-119">Notes</span></span> <br/>          | <span data-ttu-id="9b5e4-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b5e4-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9b5e4-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9b5e4-121">Structural Content</span></span>

<span data-ttu-id="9b5e4-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9b5e4-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="9b5e4-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9b5e4-123">Structure Variables</span></span>

<span data-ttu-id="9b5e4-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9b5e4-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b5e4-125">Name</span></span>                                   | <span data-ttu-id="9b5e4-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9b5e4-126">Data type</span></span>          | <span data-ttu-id="9b5e4-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="9b5e4-127">Unit</span></span>                  | <span data-ttu-id="9b5e4-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9b5e4-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="9b5e4-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="9b5e4-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5e4-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9b5e4-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9b5e4-131">string</span><span class="sxs-lookup"><span data-stu-id="9b5e4-131">string</span></span><br/>  | <span data-ttu-id="9b5e4-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="9b5e4-132">characters</span></span><br/> | <span data-ttu-id="9b5e4-133">Nombre completo válido tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="9b5e4-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="9b5e4-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9b5e4-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="9b5e4-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9b5e4-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9b5e4-137">string</span><span class="sxs-lookup"><span data-stu-id="9b5e4-137">string</span></span><br/>  | <span data-ttu-id="9b5e4-138">N/D</span><span class="sxs-lookup"><span data-stu-id="9b5e4-138">n/a</span></span><br/>        | <span data-ttu-id="9b5e4-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="9b5e4-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9b5e4-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9b5e4-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="9b5e4-142">string</span><span class="sxs-lookup"><span data-stu-id="9b5e4-142">string</span></span><br/>  | <span data-ttu-id="9b5e4-143">N/D</span><span class="sxs-lookup"><span data-stu-id="9b5e4-143">n/a</span></span><br/>        | <span data-ttu-id="9b5e4-144">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="9b5e4-145">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="9b5e4-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="9b5e4-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="9b5e4-147">integer</span><span class="sxs-lookup"><span data-stu-id="9b5e4-147">integer</span></span><br/> | <span data-ttu-id="9b5e4-148">Hojas</span><span class="sxs-lookup"><span data-stu-id="9b5e4-148">sheets</span></span><br/>     | <span data-ttu-id="9b5e4-149">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="9b5e4-150">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="9b5e4-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9b5e4-151">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9b5e4-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9b5e4-152">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9b5e4-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9b5e4-153">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9b5e4-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="9b5e4-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b5e4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b5e4-155">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9b5e4-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




