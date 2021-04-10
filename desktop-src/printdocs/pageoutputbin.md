---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bae72b69f83697cc2f482f21995acb587a2ace
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279918"
---
# <a name="pageoutputbin"></a><span data-ttu-id="6327c-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="6327c-104">PageOutputBin</span></span>

<span data-ttu-id="6327c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="6327c-105">This topic is not current.</span></span> <span data-ttu-id="6327c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6327c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6327c-107">Describe la lista completa de ubicaciones compatibles para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6327c-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="6327c-108">Permite la especificación de la ubicación de salida por página.</span><span class="sxs-lookup"><span data-stu-id="6327c-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="6327c-109">Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin se excluyen mutuamente solo se debe especificar una en un documento de funcionalidades de impresión o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6327c-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="6327c-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6327c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6327c-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6327c-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6327c-112">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="6327c-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6327c-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6327c-113">Element Information</span></span>



| <span data-ttu-id="6327c-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="6327c-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="6327c-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6327c-115">Element Type</span></span> <br/>   | <span data-ttu-id="6327c-116">Característica</span><span class="sxs-lookup"><span data-stu-id="6327c-116">Feature</span></span><br/> |
| <span data-ttu-id="6327c-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="6327c-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6327c-118">Página</span><span class="sxs-lookup"><span data-stu-id="6327c-118">Page</span></span><br/>    |
| <span data-ttu-id="6327c-119">Notas</span><span class="sxs-lookup"><span data-stu-id="6327c-119">Notes</span></span> <br/>          | <span data-ttu-id="6327c-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6327c-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6327c-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6327c-121">Structural Content</span></span>

<span data-ttu-id="6327c-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="6327c-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6327c-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="6327c-123">Structure Variables</span></span>

<span data-ttu-id="6327c-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="6327c-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6327c-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="6327c-125">Name</span></span>                                   | <span data-ttu-id="6327c-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6327c-126">Data type</span></span>          | <span data-ttu-id="6327c-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="6327c-127">Unit</span></span>                  | <span data-ttu-id="6327c-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="6327c-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6327c-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="6327c-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6327c-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6327c-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="6327c-131">string</span><span class="sxs-lookup"><span data-stu-id="6327c-131">string</span></span><br/>  | <span data-ttu-id="6327c-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="6327c-132">characters</span></span><br/> | <span data-ttu-id="6327c-133">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6327c-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6327c-134">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6327c-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6327c-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="6327c-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="6327c-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6327c-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="6327c-137">string</span><span class="sxs-lookup"><span data-stu-id="6327c-137">string</span></span><br/>  | <span data-ttu-id="6327c-138">N/D</span><span class="sxs-lookup"><span data-stu-id="6327c-138">n/a</span></span><br/>        | <span data-ttu-id="6327c-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="6327c-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6327c-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="6327c-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="6327c-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="6327c-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="6327c-142">string</span><span class="sxs-lookup"><span data-stu-id="6327c-142">string</span></span><br/>  | <span data-ttu-id="6327c-143">N/D</span><span class="sxs-lookup"><span data-stu-id="6327c-143">n/a</span></span><br/>        | <span data-ttu-id="6327c-144">FaceDownTray, FaceUpTray, buzón, clasificador, apilador, no finalizador ninguno.</span><span class="sxs-lookup"><span data-stu-id="6327c-144">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="6327c-145">Especifica el tipo general de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="6327c-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="6327c-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="6327c-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="6327c-147">integer</span><span class="sxs-lookup"><span data-stu-id="6327c-147">integer</span></span><br/> | <span data-ttu-id="6327c-148">Sheet</span><span class="sxs-lookup"><span data-stu-id="6327c-148">sheets</span></span><br/>     | <span data-ttu-id="6327c-149">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="6327c-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="6327c-150">Especifica la capacidad de los medios en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="6327c-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6327c-151">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="6327c-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6327c-152">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="6327c-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6327c-153">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="6327c-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6327c-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6327c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6327c-155">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6327c-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




