---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557a742604f6e643e8812493049b7f2b118e262c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997532"
---
# <a name="pageoutputbin"></a><span data-ttu-id="01500-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="01500-104">PageOutputBin</span></span>

<span data-ttu-id="01500-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="01500-105">This topic is not current.</span></span> <span data-ttu-id="01500-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="01500-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01500-107">Describe la lista completa de ubicaciones admitidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01500-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="01500-108">Permite la especificación de la ubicación de salida por página.</span><span class="sxs-lookup"><span data-stu-id="01500-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="01500-109">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="01500-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="01500-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="01500-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01500-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="01500-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="01500-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="01500-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="01500-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="01500-113">Element Information</span></span>



| <span data-ttu-id="01500-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="01500-114">Name</span></span> | <span data-ttu-id="01500-115">Value</span><span class="sxs-lookup"><span data-stu-id="01500-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="01500-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="01500-116">Element Type</span></span> <br/>   | <span data-ttu-id="01500-117">Característica</span><span class="sxs-lookup"><span data-stu-id="01500-117">Feature</span></span><br/> |
| <span data-ttu-id="01500-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="01500-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01500-119">Página</span><span class="sxs-lookup"><span data-stu-id="01500-119">Page</span></span><br/>    |
| <span data-ttu-id="01500-120">Notas</span><span class="sxs-lookup"><span data-stu-id="01500-120">Notes</span></span> <br/>          | <span data-ttu-id="01500-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01500-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="01500-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="01500-122">Structural Content</span></span>

<span data-ttu-id="01500-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="01500-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="01500-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="01500-124">Structure Variables</span></span>

<span data-ttu-id="01500-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="01500-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01500-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="01500-126">Name</span></span>                                   | <span data-ttu-id="01500-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="01500-127">Data type</span></span>          | <span data-ttu-id="01500-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="01500-128">Unit</span></span>                  | <span data-ttu-id="01500-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="01500-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="01500-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="01500-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01500-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="01500-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="01500-132">string</span><span class="sxs-lookup"><span data-stu-id="01500-132">string</span></span><br/>  | <span data-ttu-id="01500-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="01500-133">characters</span></span><br/> | <span data-ttu-id="01500-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="01500-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="01500-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="01500-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="01500-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="01500-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="01500-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="01500-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="01500-138">string</span><span class="sxs-lookup"><span data-stu-id="01500-138">string</span></span><br/>  | <span data-ttu-id="01500-139">N/D</span><span class="sxs-lookup"><span data-stu-id="01500-139">n/a</span></span><br/>        | <span data-ttu-id="01500-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="01500-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="01500-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="01500-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="01500-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="01500-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="01500-143">string</span><span class="sxs-lookup"><span data-stu-id="01500-143">string</span></span><br/>  | <span data-ttu-id="01500-144">N/D</span><span class="sxs-lookup"><span data-stu-id="01500-144">n/a</span></span><br/>        | <span data-ttu-id="01500-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="01500-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="01500-146">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="01500-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="01500-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="01500-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="01500-148">integer</span><span class="sxs-lookup"><span data-stu-id="01500-148">integer</span></span><br/> | <span data-ttu-id="01500-149">Hojas</span><span class="sxs-lookup"><span data-stu-id="01500-149">sheets</span></span><br/>     | <span data-ttu-id="01500-150">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="01500-150">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="01500-151">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="01500-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="01500-152">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="01500-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="01500-153">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="01500-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="01500-154">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="01500-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="01500-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01500-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01500-156">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="01500-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




