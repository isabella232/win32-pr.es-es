---
description: Obtenga información sobre el elemento JobDeviceLanguage, que describe los idiomas de dispositivo admitidos para enviar datos desde el controlador al dispositivo físico.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7bf56018a2b395ec5aa182336a89d8872057e7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408999"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="da340-103">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="da340-103">JobDeviceLanguage</span></span>

<span data-ttu-id="da340-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="da340-104">This topic is not current.</span></span> <span data-ttu-id="da340-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="da340-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="da340-106">Describe los idiomas de dispositivo admitidos para enviar datos desde el controlador al dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="da340-106">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="da340-107">A menudo se denomina "Idioma de descripción de página".</span><span class="sxs-lookup"><span data-stu-id="da340-107">This is often called "Page Description Language".</span></span> <span data-ttu-id="da340-108">Esta palabra clave define qué idioma de descripción de página es compatible con el controlador y el dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="da340-108">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="da340-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="da340-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="da340-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="da340-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="da340-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="da340-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="da340-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="da340-112">Element Information</span></span>



| <span data-ttu-id="da340-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="da340-113">Name</span></span> | <span data-ttu-id="da340-114">Valor</span><span class="sxs-lookup"><span data-stu-id="da340-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="da340-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="da340-115">Element Type</span></span> <br/>   | <span data-ttu-id="da340-116">Característica</span><span class="sxs-lookup"><span data-stu-id="da340-116">Feature</span></span><br/> |
| <span data-ttu-id="da340-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="da340-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="da340-118">Trabajo</span><span class="sxs-lookup"><span data-stu-id="da340-118">Job</span></span><br/>     |
| <span data-ttu-id="da340-119">Notas</span><span class="sxs-lookup"><span data-stu-id="da340-119">Notes</span></span> <br/>          | <span data-ttu-id="da340-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="da340-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="da340-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="da340-121">Structural Content</span></span>

<span data-ttu-id="da340-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="da340-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="da340-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="da340-123">Structure Variables</span></span>

<span data-ttu-id="da340-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="da340-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="da340-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="da340-125">Name</span></span>                                 | <span data-ttu-id="da340-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="da340-126">Data type</span></span>         | <span data-ttu-id="da340-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="da340-127">Unit</span></span>                  | <span data-ttu-id="da340-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="da340-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="da340-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="da340-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="da340-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="da340-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="da340-131">string</span><span class="sxs-lookup"><span data-stu-id="da340-131">string</span></span><br/> | <span data-ttu-id="da340-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="da340-132">characters</span></span><br/> | <span data-ttu-id="da340-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="da340-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="da340-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="da340-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="da340-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="da340-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="da340-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="da340-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="da340-137">string</span><span class="sxs-lookup"><span data-stu-id="da340-137">string</span></span><br/> | <span data-ttu-id="da340-138">N/D</span><span class="sxs-lookup"><span data-stu-id="da340-138">n/a</span></span><br/>        | <span data-ttu-id="da340-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="da340-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="da340-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="da340-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="da340-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="da340-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="da340-142">string</span><span class="sxs-lookup"><span data-stu-id="da340-142">string</span></span><br/> | <span data-ttu-id="da340-143">N/D</span><span class="sxs-lookup"><span data-stu-id="da340-143">n/a</span></span><br/>        | <span data-ttu-id="da340-144">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da340-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="da340-145">Especifica el nivel de idioma (por ejemplo, nivel 2 de PS).</span><span class="sxs-lookup"><span data-stu-id="da340-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="da340-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="da340-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="da340-147">string</span><span class="sxs-lookup"><span data-stu-id="da340-147">string</span></span><br/> | <span data-ttu-id="da340-148">N/D</span><span class="sxs-lookup"><span data-stu-id="da340-148">n/a</span></span><br/>        | <span data-ttu-id="da340-149">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da340-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="da340-150">Especifica la codificación de idioma (por ejemplo, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="da340-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="da340-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="da340-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="da340-152">string</span><span class="sxs-lookup"><span data-stu-id="da340-152">string</span></span><br/> | <span data-ttu-id="da340-153">N/D</span><span class="sxs-lookup"><span data-stu-id="da340-153">n/a</span></span><br/>        | <span data-ttu-id="da340-154">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da340-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="da340-155">Especifica la versión de idioma.</span><span class="sxs-lookup"><span data-stu-id="da340-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="da340-156">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="da340-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="da340-157">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="da340-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="da340-158">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="da340-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="da340-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da340-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da340-160">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="da340-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




