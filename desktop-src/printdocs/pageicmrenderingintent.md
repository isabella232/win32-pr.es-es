---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014213bdd2e11cc2587cef580a0b48fe03172ef0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279897"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="27e29-104">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="27e29-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="27e29-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="27e29-105">This topic is not current.</span></span> <span data-ttu-id="27e29-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="27e29-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27e29-107">Describe el intento de representación tal y como se define en la especificación de ICC V2.</span><span class="sxs-lookup"><span data-stu-id="27e29-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="27e29-108">Este valor se debe omitir si una imagen o un elemento gráfico tiene un perfil incrustado que especifica la intención de representación.</span><span class="sxs-lookup"><span data-stu-id="27e29-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="27e29-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="27e29-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27e29-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="27e29-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="27e29-111">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="27e29-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="27e29-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="27e29-112">Element Information</span></span>



| <span data-ttu-id="27e29-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="27e29-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="27e29-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="27e29-114">Element Type</span></span> <br/>   | <span data-ttu-id="27e29-115">Característica</span><span class="sxs-lookup"><span data-stu-id="27e29-115">Feature</span></span><br/> |
| <span data-ttu-id="27e29-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="27e29-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27e29-117">Página</span><span class="sxs-lookup"><span data-stu-id="27e29-117">Page</span></span><br/>    |
| <span data-ttu-id="27e29-118">Notas</span><span class="sxs-lookup"><span data-stu-id="27e29-118">Notes</span></span> <br/>          | <span data-ttu-id="27e29-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="27e29-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="27e29-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="27e29-120">Structural Content</span></span>

<span data-ttu-id="27e29-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="27e29-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="27e29-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="27e29-122">Structure Variables</span></span>

<span data-ttu-id="27e29-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="27e29-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27e29-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="27e29-124">Name</span></span>                               | <span data-ttu-id="27e29-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="27e29-125">Data type</span></span>         | <span data-ttu-id="27e29-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="27e29-126">Unit</span></span>                  | <span data-ttu-id="27e29-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="27e29-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="27e29-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="27e29-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="27e29-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="27e29-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="27e29-130">string</span><span class="sxs-lookup"><span data-stu-id="27e29-130">string</span></span><br/> | <span data-ttu-id="27e29-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="27e29-131">characters</span></span><br/> | <span data-ttu-id="27e29-132">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="27e29-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="27e29-133">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27e29-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="27e29-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="27e29-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="27e29-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="27e29-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="27e29-136">string</span><span class="sxs-lookup"><span data-stu-id="27e29-136">string</span></span><br/> | <span data-ttu-id="27e29-137">N/D</span><span class="sxs-lookup"><span data-stu-id="27e29-137">n/a</span></span><br/>        | <span data-ttu-id="27e29-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="27e29-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="27e29-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="27e29-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="27e29-140">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="27e29-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="27e29-141">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="27e29-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="27e29-142">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="27e29-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="27e29-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27e29-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27e29-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="27e29-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




