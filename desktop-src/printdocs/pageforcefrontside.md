---
description: Obtenga información sobre el elemento configurable por el usuario PageForceFrontSide. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549193"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="76e3f-105">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="76e3f-105">PageForceFrontSide</span></span>

<span data-ttu-id="76e3f-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="76e3f-106">This topic is not current.</span></span> <span data-ttu-id="76e3f-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="76e3f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="76e3f-108">Obliga a que la salida aparezca en la parte delantera de una hoja de medios.</span><span class="sxs-lookup"><span data-stu-id="76e3f-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="76e3f-109">Relevante para las hojas de medios con distintas superficies en cada lado.</span><span class="sxs-lookup"><span data-stu-id="76e3f-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="76e3f-110">En los casos en los que esta característica interfiere con las opciones de procesamiento (como DocumentDuplex), PageForceFrontSide tiene prioridad para la página específica a la que se aplica la característica.</span><span class="sxs-lookup"><span data-stu-id="76e3f-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="76e3f-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="76e3f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="76e3f-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="76e3f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="76e3f-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="76e3f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="76e3f-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="76e3f-114">Element Information</span></span>



| <span data-ttu-id="76e3f-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="76e3f-115">Name</span></span> | <span data-ttu-id="76e3f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="76e3f-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="76e3f-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="76e3f-117">Element Type</span></span> <br/>   | <span data-ttu-id="76e3f-118">Característica</span><span class="sxs-lookup"><span data-stu-id="76e3f-118">Feature</span></span><br/> |
| <span data-ttu-id="76e3f-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="76e3f-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="76e3f-120">Página</span><span class="sxs-lookup"><span data-stu-id="76e3f-120">Page</span></span><br/>    |
| <span data-ttu-id="76e3f-121">Notas</span><span class="sxs-lookup"><span data-stu-id="76e3f-121">Notes</span></span> <br/>          | <span data-ttu-id="76e3f-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="76e3f-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="76e3f-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="76e3f-123">Structural Content</span></span>

<span data-ttu-id="76e3f-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="76e3f-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="76e3f-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="76e3f-125">Structure Variables</span></span>

<span data-ttu-id="76e3f-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="76e3f-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="76e3f-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="76e3f-127">Name</span></span>                               | <span data-ttu-id="76e3f-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="76e3f-128">Data type</span></span>         | <span data-ttu-id="76e3f-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="76e3f-129">Unit</span></span>                  | <span data-ttu-id="76e3f-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="76e3f-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="76e3f-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="76e3f-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="76e3f-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="76e3f-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="76e3f-133">string</span><span class="sxs-lookup"><span data-stu-id="76e3f-133">string</span></span><br/> | <span data-ttu-id="76e3f-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="76e3f-134">characters</span></span><br/> | <span data-ttu-id="76e3f-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="76e3f-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="76e3f-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="76e3f-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="76e3f-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="76e3f-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="76e3f-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="76e3f-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="76e3f-139">string</span><span class="sxs-lookup"><span data-stu-id="76e3f-139">string</span></span><br/> | <span data-ttu-id="76e3f-140">N/D</span><span class="sxs-lookup"><span data-stu-id="76e3f-140">n/a</span></span><br/>        | <span data-ttu-id="76e3f-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="76e3f-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="76e3f-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="76e3f-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="76e3f-143">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="76e3f-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="76e3f-144">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="76e3f-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="76e3f-145">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="76e3f-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="76e3f-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76e3f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76e3f-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="76e3f-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




