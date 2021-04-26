---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d9a56e2a8a7ec74403a4b59be2a2f5d23a3a41
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995572"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="72ae9-104">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="72ae9-104">PageTrueTypeFontMode</span></span>

<span data-ttu-id="72ae9-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="72ae9-105">This topic is not current.</span></span> <span data-ttu-id="72ae9-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="72ae9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72ae9-107">Describe el método de control de fuentes TrueType que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="72ae9-107">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="72ae9-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="72ae9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72ae9-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="72ae9-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="72ae9-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="72ae9-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="72ae9-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="72ae9-111">Element Information</span></span>



| <span data-ttu-id="72ae9-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="72ae9-112">Name</span></span> | <span data-ttu-id="72ae9-113">Value</span><span class="sxs-lookup"><span data-stu-id="72ae9-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="72ae9-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="72ae9-114">Element Type</span></span> <br/>   | <span data-ttu-id="72ae9-115">Característica</span><span class="sxs-lookup"><span data-stu-id="72ae9-115">Feature</span></span><br/> |
| <span data-ttu-id="72ae9-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="72ae9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72ae9-117">Página</span><span class="sxs-lookup"><span data-stu-id="72ae9-117">Page</span></span><br/>    |
| <span data-ttu-id="72ae9-118">Notas</span><span class="sxs-lookup"><span data-stu-id="72ae9-118">Notes</span></span> <br/>          | <span data-ttu-id="72ae9-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="72ae9-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="72ae9-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="72ae9-120">Structural Content</span></span>

<span data-ttu-id="72ae9-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="72ae9-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
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

## <a name="structure-variables"></a><span data-ttu-id="72ae9-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="72ae9-122">Structure Variables</span></span>

<span data-ttu-id="72ae9-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="72ae9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72ae9-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="72ae9-124">Name</span></span>                               | <span data-ttu-id="72ae9-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="72ae9-125">Data type</span></span>         | <span data-ttu-id="72ae9-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="72ae9-126">Unit</span></span>                  | <span data-ttu-id="72ae9-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="72ae9-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="72ae9-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="72ae9-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="72ae9-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="72ae9-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="72ae9-130">string</span><span class="sxs-lookup"><span data-stu-id="72ae9-130">string</span></span><br/> | <span data-ttu-id="72ae9-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="72ae9-131">characters</span></span><br/> | <span data-ttu-id="72ae9-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="72ae9-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="72ae9-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="72ae9-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="72ae9-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="72ae9-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="72ae9-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="72ae9-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="72ae9-136">string</span><span class="sxs-lookup"><span data-stu-id="72ae9-136">string</span></span><br/> | <span data-ttu-id="72ae9-137">N/D</span><span class="sxs-lookup"><span data-stu-id="72ae9-137">n/a</span></span><br/>        | <span data-ttu-id="72ae9-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="72ae9-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="72ae9-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="72ae9-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="72ae9-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="72ae9-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="72ae9-141">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="72ae9-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="72ae9-142">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="72ae9-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="72ae9-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72ae9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72ae9-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="72ae9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




