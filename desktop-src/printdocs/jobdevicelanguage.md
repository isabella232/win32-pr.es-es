---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b9f85b44ae9fdc6efb66ce5b72bb68c5187790
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998302"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="30825-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="30825-104">JobDeviceLanguage</span></span>

<span data-ttu-id="30825-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="30825-105">This topic is not current.</span></span> <span data-ttu-id="30825-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="30825-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="30825-107">Describe los idiomas del dispositivo admitidos para enviar datos desde el controlador al dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="30825-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="30825-108">Esto se suele denominar "Idioma de descripción de página".</span><span class="sxs-lookup"><span data-stu-id="30825-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="30825-109">Esta palabra clave define qué idioma de descripción de página es compatible con el controlador y el dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="30825-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="30825-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="30825-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="30825-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="30825-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="30825-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="30825-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="30825-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="30825-113">Element Information</span></span>



| <span data-ttu-id="30825-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="30825-114">Name</span></span> | <span data-ttu-id="30825-115">Value</span><span class="sxs-lookup"><span data-stu-id="30825-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="30825-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="30825-116">Element Type</span></span> <br/>   | <span data-ttu-id="30825-117">Característica</span><span class="sxs-lookup"><span data-stu-id="30825-117">Feature</span></span><br/> |
| <span data-ttu-id="30825-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="30825-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="30825-119">Trabajo</span><span class="sxs-lookup"><span data-stu-id="30825-119">Job</span></span><br/>     |
| <span data-ttu-id="30825-120">Notas</span><span class="sxs-lookup"><span data-stu-id="30825-120">Notes</span></span> <br/>          | <span data-ttu-id="30825-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="30825-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="30825-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="30825-122">Structural Content</span></span>

<span data-ttu-id="30825-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="30825-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="30825-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="30825-124">Structure Variables</span></span>

<span data-ttu-id="30825-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="30825-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="30825-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="30825-126">Name</span></span>                                 | <span data-ttu-id="30825-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="30825-127">Data type</span></span>         | <span data-ttu-id="30825-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="30825-128">Unit</span></span>                  | <span data-ttu-id="30825-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="30825-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="30825-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="30825-130">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="30825-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="30825-131">\_OptionName\_</span></span><br/>            | <span data-ttu-id="30825-132">string</span><span class="sxs-lookup"><span data-stu-id="30825-132">string</span></span><br/> | <span data-ttu-id="30825-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="30825-133">characters</span></span><br/> | <span data-ttu-id="30825-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="30825-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="30825-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="30825-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="30825-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="30825-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="30825-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="30825-137">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="30825-138">string</span><span class="sxs-lookup"><span data-stu-id="30825-138">string</span></span><br/> | <span data-ttu-id="30825-139">N/D</span><span class="sxs-lookup"><span data-stu-id="30825-139">n/a</span></span><br/>        | <span data-ttu-id="30825-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="30825-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="30825-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="30825-141">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="30825-142">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="30825-142">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="30825-143">string</span><span class="sxs-lookup"><span data-stu-id="30825-143">string</span></span><br/> | <span data-ttu-id="30825-144">N/D</span><span class="sxs-lookup"><span data-stu-id="30825-144">n/a</span></span><br/>        | <span data-ttu-id="30825-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30825-145">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="30825-146">Especifica el nivel de idioma (por ejemplo, nivel 2 de PS).</span><span class="sxs-lookup"><span data-stu-id="30825-146">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="30825-147">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="30825-147">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="30825-148">string</span><span class="sxs-lookup"><span data-stu-id="30825-148">string</span></span><br/> | <span data-ttu-id="30825-149">N/D</span><span class="sxs-lookup"><span data-stu-id="30825-149">n/a</span></span><br/>        | <span data-ttu-id="30825-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30825-150">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="30825-151">Especifica la codificación de idioma (por ejemplo, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="30825-151">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="30825-152">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="30825-152">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="30825-153">string</span><span class="sxs-lookup"><span data-stu-id="30825-153">string</span></span><br/> | <span data-ttu-id="30825-154">N/D</span><span class="sxs-lookup"><span data-stu-id="30825-154">n/a</span></span><br/>        | <span data-ttu-id="30825-155">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30825-155">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="30825-156">Especifica la versión de idioma.</span><span class="sxs-lookup"><span data-stu-id="30825-156">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="30825-157">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="30825-157">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="30825-158">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="30825-158">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="30825-159">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="30825-159">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="30825-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30825-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30825-161">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="30825-161">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




