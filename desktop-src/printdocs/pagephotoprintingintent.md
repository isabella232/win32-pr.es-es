---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3985d6f21d0d7731d1c08d080d64a4948b58196d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104547494"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="0932b-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="0932b-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="0932b-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="0932b-105">This topic is not current.</span></span> <span data-ttu-id="0932b-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0932b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0932b-107">Indica una intención de alto nivel para el controlador con el fin de rellenar la configuración de impresión fotográfica.</span><span class="sxs-lookup"><span data-stu-id="0932b-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="0932b-108">Esta configuración trata la calidad esperada de salida que un usuario puede especificar al imprimir fotografías.</span><span class="sxs-lookup"><span data-stu-id="0932b-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="0932b-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0932b-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="0932b-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0932b-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="0932b-111">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="0932b-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0932b-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0932b-112">Element Information</span></span>



| <span data-ttu-id="0932b-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="0932b-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="0932b-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0932b-114">Element Type</span></span> <br/>   | <span data-ttu-id="0932b-115">Característica</span><span class="sxs-lookup"><span data-stu-id="0932b-115">Feature</span></span><br/> |
| <span data-ttu-id="0932b-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="0932b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0932b-117">Página</span><span class="sxs-lookup"><span data-stu-id="0932b-117">Page</span></span><br/>    |
| <span data-ttu-id="0932b-118">Notas</span><span class="sxs-lookup"><span data-stu-id="0932b-118">Notes</span></span> <br/>          | <span data-ttu-id="0932b-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0932b-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0932b-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0932b-120">Structural Content</span></span>

<span data-ttu-id="0932b-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="0932b-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0932b-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="0932b-122">Structure Variables</span></span>

<span data-ttu-id="0932b-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="0932b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0932b-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="0932b-124">Name</span></span>                               | <span data-ttu-id="0932b-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0932b-125">Data type</span></span>         | <span data-ttu-id="0932b-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="0932b-126">Unit</span></span>                  | <span data-ttu-id="0932b-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="0932b-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0932b-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="0932b-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0932b-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0932b-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0932b-130">string</span><span class="sxs-lookup"><span data-stu-id="0932b-130">string</span></span><br/> | <span data-ttu-id="0932b-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="0932b-131">characters</span></span><br/> | <span data-ttu-id="0932b-132">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0932b-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0932b-133">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0932b-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0932b-134">El nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="0932b-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="0932b-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0932b-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0932b-136">string</span><span class="sxs-lookup"><span data-stu-id="0932b-136">string</span></span><br/> | <span data-ttu-id="0932b-137">N/D</span><span class="sxs-lookup"><span data-stu-id="0932b-137">n/a</span></span><br/>        | <span data-ttu-id="0932b-138">True, False</span><span class="sxs-lookup"><span data-stu-id="0932b-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="0932b-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="0932b-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0932b-140">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="0932b-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0932b-141">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0932b-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0932b-142">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="0932b-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0932b-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0932b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0932b-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0932b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




