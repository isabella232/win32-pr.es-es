---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e357cf59bca455102f6ca29bd66bc09455ee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279910"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="80c21-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="80c21-104">PageForceFrontSide</span></span>

<span data-ttu-id="80c21-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="80c21-105">This topic is not current.</span></span> <span data-ttu-id="80c21-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="80c21-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="80c21-107">Obliga a que la salida aparezca en la parte delantera de una hoja de medios.</span><span class="sxs-lookup"><span data-stu-id="80c21-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="80c21-108">Relevante para hojas de medios con diferentes superficies en cada lado.</span><span class="sxs-lookup"><span data-stu-id="80c21-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="80c21-109">En los casos en los que esta característica interfiere con las opciones de procesamiento (como DocumentDuplex), PageForceFrontSide tiene prioridad en la página específica a la que se aplica la característica.</span><span class="sxs-lookup"><span data-stu-id="80c21-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="80c21-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="80c21-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="80c21-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="80c21-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="80c21-112">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="80c21-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="80c21-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="80c21-113">Element Information</span></span>



| <span data-ttu-id="80c21-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="80c21-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="80c21-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="80c21-115">Element Type</span></span> <br/>   | <span data-ttu-id="80c21-116">Característica</span><span class="sxs-lookup"><span data-stu-id="80c21-116">Feature</span></span><br/> |
| <span data-ttu-id="80c21-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="80c21-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="80c21-118">Página</span><span class="sxs-lookup"><span data-stu-id="80c21-118">Page</span></span><br/>    |
| <span data-ttu-id="80c21-119">Notas</span><span class="sxs-lookup"><span data-stu-id="80c21-119">Notes</span></span> <br/>          | <span data-ttu-id="80c21-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="80c21-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="80c21-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="80c21-121">Structural Content</span></span>

<span data-ttu-id="80c21-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="80c21-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="80c21-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="80c21-123">Structure Variables</span></span>

<span data-ttu-id="80c21-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="80c21-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="80c21-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="80c21-125">Name</span></span>                               | <span data-ttu-id="80c21-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="80c21-126">Data type</span></span>         | <span data-ttu-id="80c21-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="80c21-127">Unit</span></span>                  | <span data-ttu-id="80c21-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="80c21-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="80c21-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="80c21-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="80c21-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="80c21-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="80c21-131">string</span><span class="sxs-lookup"><span data-stu-id="80c21-131">string</span></span><br/> | <span data-ttu-id="80c21-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="80c21-132">characters</span></span><br/> | <span data-ttu-id="80c21-133">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="80c21-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="80c21-134">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="80c21-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="80c21-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="80c21-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="80c21-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="80c21-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="80c21-137">string</span><span class="sxs-lookup"><span data-stu-id="80c21-137">string</span></span><br/> | <span data-ttu-id="80c21-138">N/D</span><span class="sxs-lookup"><span data-stu-id="80c21-138">n/a</span></span><br/>        | <span data-ttu-id="80c21-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="80c21-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="80c21-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="80c21-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="80c21-141">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="80c21-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="80c21-142">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="80c21-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="80c21-143">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="80c21-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="80c21-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80c21-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c21-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="80c21-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




