---
description: Obtenga información sobre el elemento configurable por el usuario PageMediaColor. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3041c8954048f60f52e9324f0c6565396d7fafe2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549163"
---
# <a name="pagemediacolor"></a><span data-ttu-id="224c8-105">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="224c8-105">PageMediaColor</span></span>

<span data-ttu-id="224c8-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="224c8-106">This topic is not current.</span></span> <span data-ttu-id="224c8-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="224c8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="224c8-108">Describe las opciones color multimedia y las características de cada opción.</span><span class="sxs-lookup"><span data-stu-id="224c8-108">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="224c8-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="224c8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="224c8-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="224c8-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="224c8-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="224c8-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="224c8-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="224c8-112">Element Information</span></span>



| <span data-ttu-id="224c8-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="224c8-113">Name</span></span> | <span data-ttu-id="224c8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="224c8-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="224c8-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="224c8-115">Element Type</span></span> <br/>   | <span data-ttu-id="224c8-116">Característica</span><span class="sxs-lookup"><span data-stu-id="224c8-116">Feature</span></span><br/> |
| <span data-ttu-id="224c8-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="224c8-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="224c8-118">Página</span><span class="sxs-lookup"><span data-stu-id="224c8-118">Page</span></span><br/>    |
| <span data-ttu-id="224c8-119">Notas</span><span class="sxs-lookup"><span data-stu-id="224c8-119">Notes</span></span> <br/>          | <span data-ttu-id="224c8-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="224c8-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="224c8-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="224c8-121">Structural Content</span></span>

<span data-ttu-id="224c8-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="224c8-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="224c8-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="224c8-123">Structure Variables</span></span>

<span data-ttu-id="224c8-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="224c8-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="224c8-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="224c8-125">Name</span></span>                               | <span data-ttu-id="224c8-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="224c8-126">Data type</span></span>         | <span data-ttu-id="224c8-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="224c8-127">Unit</span></span>                  | <span data-ttu-id="224c8-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="224c8-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="224c8-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="224c8-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="224c8-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="224c8-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="224c8-131">string</span><span class="sxs-lookup"><span data-stu-id="224c8-131">string</span></span><br/> | <span data-ttu-id="224c8-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="224c8-132">characters</span></span><br/> | <span data-ttu-id="224c8-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="224c8-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="224c8-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="224c8-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="224c8-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="224c8-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="224c8-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="224c8-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="224c8-137">string</span><span class="sxs-lookup"><span data-stu-id="224c8-137">string</span></span><br/> | <span data-ttu-id="224c8-138">N/D</span><span class="sxs-lookup"><span data-stu-id="224c8-138">n/a</span></span><br/>        | <span data-ttu-id="224c8-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="224c8-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="224c8-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="224c8-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="224c8-141">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="224c8-141">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="224c8-142">string</span><span class="sxs-lookup"><span data-stu-id="224c8-142">string</span></span><br/> | <span data-ttu-id="224c8-143">sRGB Color</span><span class="sxs-lookup"><span data-stu-id="224c8-143">sRGB Color</span></span><br/> | <span data-ttu-id="224c8-144">\#AARRGGBB donde A, R, G, B representan dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="224c8-144">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="224c8-145">Define el color sRGB de la hoja de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="224c8-145">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="224c8-146">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="224c8-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="224c8-147">Las palabras clave del esquema de impresión público se definen en el espacio de `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` nombres .</span><span class="sxs-lookup"><span data-stu-id="224c8-147">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="224c8-148">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="224c8-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="224c8-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="224c8-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="224c8-150">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="224c8-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
