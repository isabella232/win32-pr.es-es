---
description: Revise el elemento PagePhotoPrintingIntent configurable por el usuario. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1cf9ae587062efc68b953f5931b55147940b1b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548983"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="afbf3-105">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="afbf3-105">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="afbf3-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="afbf3-106">This topic is not current.</span></span> <span data-ttu-id="afbf3-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="afbf3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="afbf3-108">Indica una intención de alto nivel al controlador para la población de la configuración de impresión de fotos.</span><span class="sxs-lookup"><span data-stu-id="afbf3-108">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="afbf3-109">Esta configuración trata con la calidad de salida esperada que un usuario puede especificar al imprimir fotos.</span><span class="sxs-lookup"><span data-stu-id="afbf3-109">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="afbf3-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="afbf3-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="afbf3-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="afbf3-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="afbf3-112">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="afbf3-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="afbf3-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="afbf3-113">Element Information</span></span>



| <span data-ttu-id="afbf3-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="afbf3-114">Name</span></span> | <span data-ttu-id="afbf3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="afbf3-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="afbf3-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="afbf3-116">Element Type</span></span> <br/>   | <span data-ttu-id="afbf3-117">Característica</span><span class="sxs-lookup"><span data-stu-id="afbf3-117">Feature</span></span><br/> |
| <span data-ttu-id="afbf3-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="afbf3-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="afbf3-119">Página</span><span class="sxs-lookup"><span data-stu-id="afbf3-119">Page</span></span><br/>    |
| <span data-ttu-id="afbf3-120">Notas</span><span class="sxs-lookup"><span data-stu-id="afbf3-120">Notes</span></span> <br/>          | <span data-ttu-id="afbf3-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="afbf3-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="afbf3-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="afbf3-122">Structural Content</span></span>

<span data-ttu-id="afbf3-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="afbf3-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="afbf3-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="afbf3-124">Structure Variables</span></span>

<span data-ttu-id="afbf3-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="afbf3-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="afbf3-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="afbf3-126">Name</span></span>                               | <span data-ttu-id="afbf3-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="afbf3-127">Data type</span></span>         | <span data-ttu-id="afbf3-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="afbf3-128">Unit</span></span>                  | <span data-ttu-id="afbf3-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="afbf3-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="afbf3-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="afbf3-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="afbf3-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="afbf3-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="afbf3-132">string</span><span class="sxs-lookup"><span data-stu-id="afbf3-132">string</span></span><br/> | <span data-ttu-id="afbf3-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="afbf3-133">characters</span></span><br/> | <span data-ttu-id="afbf3-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="afbf3-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="afbf3-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="afbf3-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="afbf3-136">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="afbf3-136">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="afbf3-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="afbf3-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="afbf3-138">string</span><span class="sxs-lookup"><span data-stu-id="afbf3-138">string</span></span><br/> | <span data-ttu-id="afbf3-139">N/D</span><span class="sxs-lookup"><span data-stu-id="afbf3-139">n/a</span></span><br/>        | <span data-ttu-id="afbf3-140">True, False</span><span class="sxs-lookup"><span data-stu-id="afbf3-140">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="afbf3-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="afbf3-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="afbf3-142">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="afbf3-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="afbf3-143">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="afbf3-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="afbf3-144">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="afbf3-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="afbf3-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="afbf3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afbf3-146">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="afbf3-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




