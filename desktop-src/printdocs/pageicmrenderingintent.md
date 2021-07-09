---
description: Obtenga información sobre el elemento PageICMRenderingIntent configurable por el usuario. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549183"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="b3694-105">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="b3694-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="b3694-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="b3694-106">This topic is not current.</span></span> <span data-ttu-id="b3694-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b3694-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b3694-108">Describe la intención de representación tal como se define en la especificación de LAV V2.</span><span class="sxs-lookup"><span data-stu-id="b3694-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="b3694-109">Este valor debe omitirse si una imagen o un elemento gráfico tiene un perfil incrustado que especifica la intención Rendering.</span><span class="sxs-lookup"><span data-stu-id="b3694-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="b3694-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b3694-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b3694-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="b3694-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b3694-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b3694-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b3694-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b3694-113">Element Information</span></span>



| <span data-ttu-id="b3694-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="b3694-114">Name</span></span> | <span data-ttu-id="b3694-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b3694-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b3694-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b3694-116">Element Type</span></span> <br/>   | <span data-ttu-id="b3694-117">Característica</span><span class="sxs-lookup"><span data-stu-id="b3694-117">Feature</span></span><br/> |
| <span data-ttu-id="b3694-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="b3694-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b3694-119">Página</span><span class="sxs-lookup"><span data-stu-id="b3694-119">Page</span></span><br/>    |
| <span data-ttu-id="b3694-120">Notas</span><span class="sxs-lookup"><span data-stu-id="b3694-120">Notes</span></span> <br/>          | <span data-ttu-id="b3694-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b3694-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="b3694-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="b3694-122">Structural Content</span></span>

<span data-ttu-id="b3694-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="b3694-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b3694-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="b3694-124">Structure Variables</span></span>

<span data-ttu-id="b3694-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="b3694-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b3694-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="b3694-126">Name</span></span>                               | <span data-ttu-id="b3694-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b3694-127">Data type</span></span>         | <span data-ttu-id="b3694-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="b3694-128">Unit</span></span>                  | <span data-ttu-id="b3694-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="b3694-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b3694-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="b3694-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b3694-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b3694-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b3694-132">string</span><span class="sxs-lookup"><span data-stu-id="b3694-132">string</span></span><br/> | <span data-ttu-id="b3694-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="b3694-133">characters</span></span><br/> | <span data-ttu-id="b3694-134">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b3694-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b3694-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b3694-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b3694-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="b3694-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b3694-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b3694-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b3694-138">string</span><span class="sxs-lookup"><span data-stu-id="b3694-138">string</span></span><br/> | <span data-ttu-id="b3694-139">N/D</span><span class="sxs-lookup"><span data-stu-id="b3694-139">n/a</span></span><br/>        | <span data-ttu-id="b3694-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="b3694-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b3694-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="b3694-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b3694-142">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b3694-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b3694-143">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="b3694-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b3694-144">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="b3694-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b3694-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3694-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3694-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b3694-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




