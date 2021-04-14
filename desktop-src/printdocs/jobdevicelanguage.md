---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5b128cd8a0bd06cc259d3da0daf834f3c2aebf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361994"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="9607d-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="9607d-104">JobDeviceLanguage</span></span>

<span data-ttu-id="9607d-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="9607d-105">This topic is not current.</span></span> <span data-ttu-id="9607d-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9607d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9607d-107">Describe los idiomas de dispositivo admitidos para enviar datos de un controlador a un dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="9607d-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="9607d-108">Esto se suele denominar "lenguaje de descripción de páginas".</span><span class="sxs-lookup"><span data-stu-id="9607d-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="9607d-109">Esta palabra clave define qué lenguaje de descripción de página es compatible con el controlador y el dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="9607d-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="9607d-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9607d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9607d-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9607d-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9607d-112">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="9607d-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9607d-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9607d-113">Element Information</span></span>



| <span data-ttu-id="9607d-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="9607d-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="9607d-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9607d-115">Element Type</span></span> <br/>   | <span data-ttu-id="9607d-116">Característica</span><span class="sxs-lookup"><span data-stu-id="9607d-116">Feature</span></span><br/> |
| <span data-ttu-id="9607d-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9607d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9607d-118">Trabajo</span><span class="sxs-lookup"><span data-stu-id="9607d-118">Job</span></span><br/>     |
| <span data-ttu-id="9607d-119">Notas</span><span class="sxs-lookup"><span data-stu-id="9607d-119">Notes</span></span> <br/>          | <span data-ttu-id="9607d-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9607d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9607d-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9607d-121">Structural Content</span></span>

<span data-ttu-id="9607d-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9607d-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9607d-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9607d-123">Structure Variables</span></span>

<span data-ttu-id="9607d-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9607d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9607d-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="9607d-125">Name</span></span>                                 | <span data-ttu-id="9607d-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9607d-126">Data type</span></span>         | <span data-ttu-id="9607d-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="9607d-127">Unit</span></span>                  | <span data-ttu-id="9607d-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9607d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9607d-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="9607d-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9607d-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9607d-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="9607d-131">string</span><span class="sxs-lookup"><span data-stu-id="9607d-131">string</span></span><br/> | <span data-ttu-id="9607d-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="9607d-132">characters</span></span><br/> | <span data-ttu-id="9607d-133">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9607d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9607d-134">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9607d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9607d-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9607d-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9607d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9607d-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="9607d-137">string</span><span class="sxs-lookup"><span data-stu-id="9607d-137">string</span></span><br/> | <span data-ttu-id="9607d-138">N/D</span><span class="sxs-lookup"><span data-stu-id="9607d-138">n/a</span></span><br/>        | <span data-ttu-id="9607d-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="9607d-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9607d-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9607d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="9607d-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="9607d-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="9607d-142">string</span><span class="sxs-lookup"><span data-stu-id="9607d-142">string</span></span><br/> | <span data-ttu-id="9607d-143">N/D</span><span class="sxs-lookup"><span data-stu-id="9607d-143">n/a</span></span><br/>        | <span data-ttu-id="9607d-144">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9607d-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="9607d-145">Especifica el nivel de idioma (por ejemplo, PS de nivel 2).</span><span class="sxs-lookup"><span data-stu-id="9607d-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="9607d-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="9607d-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="9607d-147">string</span><span class="sxs-lookup"><span data-stu-id="9607d-147">string</span></span><br/> | <span data-ttu-id="9607d-148">N/D</span><span class="sxs-lookup"><span data-stu-id="9607d-148">n/a</span></span><br/>        | <span data-ttu-id="9607d-149">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9607d-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="9607d-150">Especifica la codificación de idioma (por ejemplo, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="9607d-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="9607d-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="9607d-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="9607d-152">string</span><span class="sxs-lookup"><span data-stu-id="9607d-152">string</span></span><br/> | <span data-ttu-id="9607d-153">N/D</span><span class="sxs-lookup"><span data-stu-id="9607d-153">n/a</span></span><br/>        | <span data-ttu-id="9607d-154">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9607d-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="9607d-155">Especifica la versión de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="9607d-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9607d-156">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="9607d-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9607d-157">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9607d-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9607d-158">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9607d-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9607d-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9607d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9607d-160">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9607d-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




