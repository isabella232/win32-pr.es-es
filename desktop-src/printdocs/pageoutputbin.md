---
description: Obtenga información sobre el elemento configurable por el usuario PageOutputBin. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9963bf2ca7a2dd60be37c797a27c6ff09b1206
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549003"
---
# <a name="pageoutputbin"></a><span data-ttu-id="8f131-105">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="8f131-105">PageOutputBin</span></span>

<span data-ttu-id="8f131-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="8f131-106">This topic is not current.</span></span> <span data-ttu-id="8f131-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f131-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f131-108">Describe la lista completa de ubicaciones admitidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f131-108">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="8f131-109">Permite la especificación de la ubicación de salida por página.</span><span class="sxs-lookup"><span data-stu-id="8f131-109">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="8f131-110">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="8f131-110">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="8f131-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8f131-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8f131-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="8f131-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8f131-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8f131-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8f131-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8f131-114">Element Information</span></span>



| <span data-ttu-id="8f131-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f131-115">Name</span></span> | <span data-ttu-id="8f131-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8f131-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8f131-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8f131-117">Element Type</span></span> <br/>   | <span data-ttu-id="8f131-118">Característica</span><span class="sxs-lookup"><span data-stu-id="8f131-118">Feature</span></span><br/> |
| <span data-ttu-id="8f131-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="8f131-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8f131-120">Página</span><span class="sxs-lookup"><span data-stu-id="8f131-120">Page</span></span><br/>    |
| <span data-ttu-id="8f131-121">Notas</span><span class="sxs-lookup"><span data-stu-id="8f131-121">Notes</span></span> <br/>          | <span data-ttu-id="8f131-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8f131-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="8f131-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="8f131-123">Structural Content</span></span>

<span data-ttu-id="8f131-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="8f131-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="8f131-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="8f131-125">Structure Variables</span></span>

<span data-ttu-id="8f131-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="8f131-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8f131-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f131-127">Name</span></span>                                   | <span data-ttu-id="8f131-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f131-128">Data type</span></span>          | <span data-ttu-id="8f131-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="8f131-129">Unit</span></span>                  | <span data-ttu-id="8f131-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="8f131-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8f131-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="8f131-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f131-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8f131-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="8f131-133">string</span><span class="sxs-lookup"><span data-stu-id="8f131-133">string</span></span><br/>  | <span data-ttu-id="8f131-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="8f131-134">characters</span></span><br/> | <span data-ttu-id="8f131-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="8f131-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8f131-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f131-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8f131-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="8f131-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="8f131-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8f131-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="8f131-139">string</span><span class="sxs-lookup"><span data-stu-id="8f131-139">string</span></span><br/>  | <span data-ttu-id="8f131-140">N/D</span><span class="sxs-lookup"><span data-stu-id="8f131-140">n/a</span></span><br/>        | <span data-ttu-id="8f131-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="8f131-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8f131-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="8f131-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="8f131-143">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="8f131-143">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="8f131-144">string</span><span class="sxs-lookup"><span data-stu-id="8f131-144">string</span></span><br/>  | <span data-ttu-id="8f131-145">N/D</span><span class="sxs-lookup"><span data-stu-id="8f131-145">n/a</span></span><br/>        | <span data-ttu-id="8f131-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="8f131-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="8f131-147">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="8f131-147">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="8f131-148">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="8f131-148">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="8f131-149">integer</span><span class="sxs-lookup"><span data-stu-id="8f131-149">integer</span></span><br/> | <span data-ttu-id="8f131-150">Hojas</span><span class="sxs-lookup"><span data-stu-id="8f131-150">sheets</span></span><br/>     | <span data-ttu-id="8f131-151">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="8f131-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="8f131-152">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="8f131-152">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8f131-153">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8f131-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8f131-154">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="8f131-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8f131-155">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="8f131-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="related-topics"></a><span data-ttu-id="8f131-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f131-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f131-157">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8f131-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




