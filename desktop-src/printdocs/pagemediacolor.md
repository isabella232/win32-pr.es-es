---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc6d39d3b189edbd2bd51803f1bb517fedd3edf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105649341"
---
# <a name="pagemediacolor"></a><span data-ttu-id="54a19-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="54a19-104">PageMediaColor</span></span>

<span data-ttu-id="54a19-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="54a19-105">This topic is not current.</span></span> <span data-ttu-id="54a19-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="54a19-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54a19-107">Describe las opciones de color de los medios y las características de cada opción.</span><span class="sxs-lookup"><span data-stu-id="54a19-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="54a19-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="54a19-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="54a19-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="54a19-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="54a19-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="54a19-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="54a19-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="54a19-111">Element Information</span></span>



| <span data-ttu-id="54a19-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="54a19-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="54a19-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="54a19-113">Element Type</span></span> <br/>   | <span data-ttu-id="54a19-114">Característica</span><span class="sxs-lookup"><span data-stu-id="54a19-114">Feature</span></span><br/> |
| <span data-ttu-id="54a19-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="54a19-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="54a19-116">Página</span><span class="sxs-lookup"><span data-stu-id="54a19-116">Page</span></span><br/>    |
| <span data-ttu-id="54a19-117">Notas</span><span class="sxs-lookup"><span data-stu-id="54a19-117">Notes</span></span> <br/>          | <span data-ttu-id="54a19-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="54a19-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="54a19-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="54a19-119">Structural Content</span></span>

<span data-ttu-id="54a19-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="54a19-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="54a19-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="54a19-121">Structure Variables</span></span>

<span data-ttu-id="54a19-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="54a19-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="54a19-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="54a19-123">Name</span></span>                               | <span data-ttu-id="54a19-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="54a19-124">Data type</span></span>         | <span data-ttu-id="54a19-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="54a19-125">Unit</span></span>                  | <span data-ttu-id="54a19-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="54a19-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="54a19-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="54a19-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="54a19-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="54a19-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="54a19-129">string</span><span class="sxs-lookup"><span data-stu-id="54a19-129">string</span></span><br/> | <span data-ttu-id="54a19-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="54a19-130">characters</span></span><br/> | <span data-ttu-id="54a19-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="54a19-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="54a19-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="54a19-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="54a19-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="54a19-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="54a19-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="54a19-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="54a19-135">string</span><span class="sxs-lookup"><span data-stu-id="54a19-135">string</span></span><br/> | <span data-ttu-id="54a19-136">N/D</span><span class="sxs-lookup"><span data-stu-id="54a19-136">n/a</span></span><br/>        | <span data-ttu-id="54a19-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="54a19-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="54a19-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="54a19-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="54a19-139">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="54a19-139">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="54a19-140">string</span><span class="sxs-lookup"><span data-stu-id="54a19-140">string</span></span><br/> | <span data-ttu-id="54a19-141">Color sRGB</span><span class="sxs-lookup"><span data-stu-id="54a19-141">sRGB Color</span></span><br/> | <span data-ttu-id="54a19-142">\#AARRGGBB, donde A, R, G, B representan dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="54a19-142">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="54a19-143">Define el color sRGB de la hoja de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="54a19-143">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="54a19-144">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="54a19-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="54a19-145">Las palabras clave del esquema de impresión público se definen en el `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="54a19-145">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="54a19-146">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="54a19-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="54a19-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54a19-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54a19-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="54a19-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
