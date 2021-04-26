---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e363050034137bcfb3ff2b779ecda05200865312
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996942"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="822b3-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="822b3-104">PageForceFrontSide</span></span>

<span data-ttu-id="822b3-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="822b3-105">This topic is not current.</span></span> <span data-ttu-id="822b3-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="822b3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="822b3-107">Obliga a que la salida aparezca en la parte delantera de una hoja de medios.</span><span class="sxs-lookup"><span data-stu-id="822b3-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="822b3-108">Relevante para las hojas de medios con distintas superficies en cada lado.</span><span class="sxs-lookup"><span data-stu-id="822b3-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="822b3-109">En los casos en los que esta característica interfiere con las opciones de procesamiento (como DocumentDuplex), PageForceFrontSide tiene prioridad para la página específica a la que se aplica la característica.</span><span class="sxs-lookup"><span data-stu-id="822b3-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="822b3-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="822b3-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="822b3-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="822b3-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="822b3-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="822b3-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="822b3-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="822b3-113">Element Information</span></span>



| <span data-ttu-id="822b3-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="822b3-114">Name</span></span> | <span data-ttu-id="822b3-115">Value</span><span class="sxs-lookup"><span data-stu-id="822b3-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="822b3-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="822b3-116">Element Type</span></span> <br/>   | <span data-ttu-id="822b3-117">Característica</span><span class="sxs-lookup"><span data-stu-id="822b3-117">Feature</span></span><br/> |
| <span data-ttu-id="822b3-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="822b3-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="822b3-119">Página</span><span class="sxs-lookup"><span data-stu-id="822b3-119">Page</span></span><br/>    |
| <span data-ttu-id="822b3-120">Notas</span><span class="sxs-lookup"><span data-stu-id="822b3-120">Notes</span></span> <br/>          | <span data-ttu-id="822b3-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="822b3-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="822b3-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="822b3-122">Structural Content</span></span>

<span data-ttu-id="822b3-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="822b3-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="822b3-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="822b3-124">Structure Variables</span></span>

<span data-ttu-id="822b3-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="822b3-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="822b3-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="822b3-126">Name</span></span>                               | <span data-ttu-id="822b3-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="822b3-127">Data type</span></span>         | <span data-ttu-id="822b3-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="822b3-128">Unit</span></span>                  | <span data-ttu-id="822b3-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="822b3-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="822b3-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="822b3-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="822b3-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="822b3-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="822b3-132">string</span><span class="sxs-lookup"><span data-stu-id="822b3-132">string</span></span><br/> | <span data-ttu-id="822b3-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="822b3-133">characters</span></span><br/> | <span data-ttu-id="822b3-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="822b3-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="822b3-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="822b3-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="822b3-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="822b3-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="822b3-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="822b3-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="822b3-138">string</span><span class="sxs-lookup"><span data-stu-id="822b3-138">string</span></span><br/> | <span data-ttu-id="822b3-139">N/D</span><span class="sxs-lookup"><span data-stu-id="822b3-139">n/a</span></span><br/>        | <span data-ttu-id="822b3-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="822b3-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="822b3-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="822b3-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="822b3-142">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="822b3-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="822b3-143">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="822b3-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="822b3-144">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="822b3-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="822b3-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="822b3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="822b3-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="822b3-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




