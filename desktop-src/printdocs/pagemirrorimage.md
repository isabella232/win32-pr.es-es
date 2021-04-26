---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: a05357c0-6a82-42ff-b4f8-d3e0ee089055
title: PageMirrorImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d9fe0a82ad14c149849c3bf6bf0c5de6144571
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994472"
---
# <a name="pagemirrorimage"></a><span data-ttu-id="c41c8-104">PageMirrorImage</span><span class="sxs-lookup"><span data-stu-id="c41c8-104">PageMirrorImage</span></span>

<span data-ttu-id="c41c8-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="c41c8-105">This topic is not current.</span></span> <span data-ttu-id="c41c8-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c41c8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c41c8-107">Describe la configuración de creación de reflejo de la salida.</span><span class="sxs-lookup"><span data-stu-id="c41c8-107">Describes the mirroring setting of the output.</span></span>

-   [<span data-ttu-id="c41c8-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c41c8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c41c8-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c41c8-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c41c8-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c41c8-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c41c8-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c41c8-111">Element Information</span></span>



| <span data-ttu-id="c41c8-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="c41c8-112">Name</span></span> | <span data-ttu-id="c41c8-113">Value</span><span class="sxs-lookup"><span data-stu-id="c41c8-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c41c8-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c41c8-114">Element Type</span></span> <br/>   | <span data-ttu-id="c41c8-115">Característica</span><span class="sxs-lookup"><span data-stu-id="c41c8-115">Feature</span></span><br/> |
| <span data-ttu-id="c41c8-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="c41c8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c41c8-117">Página</span><span class="sxs-lookup"><span data-stu-id="c41c8-117">Page</span></span><br/>    |
| <span data-ttu-id="c41c8-118">Notas</span><span class="sxs-lookup"><span data-stu-id="c41c8-118">Notes</span></span> <br/>          | <span data-ttu-id="c41c8-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c41c8-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c41c8-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c41c8-120">Structural Content</span></span>

<span data-ttu-id="c41c8-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="c41c8-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
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

## <a name="structure-variables"></a><span data-ttu-id="c41c8-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="c41c8-122">Structure Variables</span></span>

<span data-ttu-id="c41c8-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="c41c8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c41c8-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="c41c8-124">Name</span></span>                               | <span data-ttu-id="c41c8-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c41c8-125">Data type</span></span>         | <span data-ttu-id="c41c8-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="c41c8-126">Unit</span></span>                  | <span data-ttu-id="c41c8-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="c41c8-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c41c8-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="c41c8-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c41c8-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c41c8-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c41c8-130">string</span><span class="sxs-lookup"><span data-stu-id="c41c8-130">string</span></span><br/> | <span data-ttu-id="c41c8-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="c41c8-131">characters</span></span><br/> | <span data-ttu-id="c41c8-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c41c8-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c41c8-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c41c8-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c41c8-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="c41c8-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c41c8-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c41c8-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c41c8-136">string</span><span class="sxs-lookup"><span data-stu-id="c41c8-136">string</span></span><br/> | <span data-ttu-id="c41c8-137">N/D</span><span class="sxs-lookup"><span data-stu-id="c41c8-137">n/a</span></span><br/>        | <span data-ttu-id="c41c8-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="c41c8-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c41c8-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="c41c8-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c41c8-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c41c8-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c41c8-141">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="c41c8-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c41c8-142">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="c41c8-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be mirrored parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:MirrorImageWidth" />
  <!-- Specifies the output should be mirrored parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:MirrorImageHeight" />
  <!-- Specifies the output should not be mirrored. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c41c8-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c41c8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c41c8-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c41c8-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




