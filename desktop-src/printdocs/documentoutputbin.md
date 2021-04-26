---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6d16ca000e76b01cd2c3165054d7acc81351b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997142"
---
# <a name="documentoutputbin"></a><span data-ttu-id="15b2d-104">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="15b2d-104">DocumentOutputBin</span></span>

<span data-ttu-id="15b2d-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="15b2d-105">This topic is not current.</span></span> <span data-ttu-id="15b2d-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="15b2d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15b2d-107">Describe la lista completa de ubicaciones admitidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b2d-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="15b2d-108">Permite la especificación de la ubicación de salida por documento.</span><span class="sxs-lookup"><span data-stu-id="15b2d-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="15b2d-109">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="15b2d-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="15b2d-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="15b2d-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="15b2d-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="15b2d-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="15b2d-112">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="15b2d-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="15b2d-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="15b2d-113">Element Information</span></span>



| <span data-ttu-id="15b2d-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="15b2d-114">Name</span></span> | <span data-ttu-id="15b2d-115">Value</span><span class="sxs-lookup"><span data-stu-id="15b2d-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="15b2d-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="15b2d-116">Element Type</span></span> <br/>   | <span data-ttu-id="15b2d-117">Característica</span><span class="sxs-lookup"><span data-stu-id="15b2d-117">Feature</span></span><br/>  |
| <span data-ttu-id="15b2d-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="15b2d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15b2d-119">Documento</span><span class="sxs-lookup"><span data-stu-id="15b2d-119">Document</span></span><br/> |
| <span data-ttu-id="15b2d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="15b2d-120">Notes</span></span> <br/>          | <span data-ttu-id="15b2d-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="15b2d-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="15b2d-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="15b2d-122">Structural Content</span></span>

<span data-ttu-id="15b2d-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="15b2d-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="15b2d-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="15b2d-124">Structure Variables</span></span>

<span data-ttu-id="15b2d-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="15b2d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15b2d-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="15b2d-126">Name</span></span>                                   | <span data-ttu-id="15b2d-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="15b2d-127">Data type</span></span>          | <span data-ttu-id="15b2d-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="15b2d-128">Unit</span></span>                  | <span data-ttu-id="15b2d-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="15b2d-129">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="15b2d-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="15b2d-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15b2d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="15b2d-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="15b2d-132">string</span><span class="sxs-lookup"><span data-stu-id="15b2d-132">string</span></span><br/>  | <span data-ttu-id="15b2d-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="15b2d-133">characters</span></span><br/> | <span data-ttu-id="15b2d-134">Nombre completo válido tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="15b2d-134">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="15b2d-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="15b2d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="15b2d-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="15b2d-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="15b2d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="15b2d-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="15b2d-138">string</span><span class="sxs-lookup"><span data-stu-id="15b2d-138">string</span></span><br/>  | <span data-ttu-id="15b2d-139">N/D</span><span class="sxs-lookup"><span data-stu-id="15b2d-139">n/a</span></span><br/>        | <span data-ttu-id="15b2d-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="15b2d-140">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="15b2d-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="15b2d-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="15b2d-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="15b2d-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="15b2d-143">string</span><span class="sxs-lookup"><span data-stu-id="15b2d-143">string</span></span><br/>  | <span data-ttu-id="15b2d-144">N/D</span><span class="sxs-lookup"><span data-stu-id="15b2d-144">n/a</span></span><br/>        | <span data-ttu-id="15b2d-145">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="15b2d-145">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="15b2d-146">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="15b2d-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="15b2d-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="15b2d-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="15b2d-148">integer</span><span class="sxs-lookup"><span data-stu-id="15b2d-148">integer</span></span><br/> | <span data-ttu-id="15b2d-149">Hojas</span><span class="sxs-lookup"><span data-stu-id="15b2d-149">sheets</span></span><br/>     | <span data-ttu-id="15b2d-150">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="15b2d-150">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="15b2d-151">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="15b2d-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="15b2d-152">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="15b2d-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="15b2d-153">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="15b2d-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="15b2d-154">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="15b2d-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="15b2d-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15b2d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b2d-156">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="15b2d-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




