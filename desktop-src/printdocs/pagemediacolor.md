---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c9a314bf435664d121fd35e588b62903da323e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994512"
---
# <a name="pagemediacolor"></a><span data-ttu-id="05b67-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="05b67-104">PageMediaColor</span></span>

<span data-ttu-id="05b67-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="05b67-105">This topic is not current.</span></span> <span data-ttu-id="05b67-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="05b67-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="05b67-107">Describe las opciones color multimedia y las características de cada opción.</span><span class="sxs-lookup"><span data-stu-id="05b67-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="05b67-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="05b67-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="05b67-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="05b67-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="05b67-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="05b67-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="05b67-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="05b67-111">Element Information</span></span>



| <span data-ttu-id="05b67-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="05b67-112">Name</span></span> | <span data-ttu-id="05b67-113">Value</span><span class="sxs-lookup"><span data-stu-id="05b67-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="05b67-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="05b67-114">Element Type</span></span> <br/>   | <span data-ttu-id="05b67-115">Característica</span><span class="sxs-lookup"><span data-stu-id="05b67-115">Feature</span></span><br/> |
| <span data-ttu-id="05b67-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="05b67-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="05b67-117">Página</span><span class="sxs-lookup"><span data-stu-id="05b67-117">Page</span></span><br/>    |
| <span data-ttu-id="05b67-118">Notas</span><span class="sxs-lookup"><span data-stu-id="05b67-118">Notes</span></span> <br/>          | <span data-ttu-id="05b67-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="05b67-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="05b67-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="05b67-120">Structural Content</span></span>

<span data-ttu-id="05b67-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="05b67-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="05b67-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="05b67-122">Structure Variables</span></span>

<span data-ttu-id="05b67-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="05b67-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="05b67-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="05b67-124">Name</span></span>                               | <span data-ttu-id="05b67-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="05b67-125">Data type</span></span>         | <span data-ttu-id="05b67-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="05b67-126">Unit</span></span>                  | <span data-ttu-id="05b67-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="05b67-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="05b67-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="05b67-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="05b67-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="05b67-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="05b67-130">string</span><span class="sxs-lookup"><span data-stu-id="05b67-130">string</span></span><br/> | <span data-ttu-id="05b67-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="05b67-131">characters</span></span><br/> | <span data-ttu-id="05b67-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="05b67-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="05b67-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05b67-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="05b67-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="05b67-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="05b67-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="05b67-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="05b67-136">string</span><span class="sxs-lookup"><span data-stu-id="05b67-136">string</span></span><br/> | <span data-ttu-id="05b67-137">N/D</span><span class="sxs-lookup"><span data-stu-id="05b67-137">n/a</span></span><br/>        | <span data-ttu-id="05b67-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="05b67-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="05b67-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="05b67-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="05b67-140">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="05b67-140">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="05b67-141">string</span><span class="sxs-lookup"><span data-stu-id="05b67-141">string</span></span><br/> | <span data-ttu-id="05b67-142">sRGB Color</span><span class="sxs-lookup"><span data-stu-id="05b67-142">sRGB Color</span></span><br/> | <span data-ttu-id="05b67-143">\#AARRGGBB donde A, R, G, B representan dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="05b67-143">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="05b67-144">Define el color sRGB de la hoja de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="05b67-144">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="05b67-145">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="05b67-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="05b67-146">Las palabras clave de esquema de impresión públicas se definen en el espacio de `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` nombres .</span><span class="sxs-lookup"><span data-stu-id="05b67-146">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="05b67-147">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="05b67-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="05b67-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05b67-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05b67-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="05b67-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
