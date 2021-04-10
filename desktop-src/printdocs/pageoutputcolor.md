---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279917"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="d1fdb-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="d1fdb-104">PageOutputColor</span></span>

<span data-ttu-id="d1fdb-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-105">This topic is not current.</span></span> <span data-ttu-id="d1fdb-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d1fdb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d1fdb-107">Describe las características de la configuración de color de la salida.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="d1fdb-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d1fdb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d1fdb-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d1fdb-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d1fdb-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="d1fdb-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d1fdb-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d1fdb-111">Element Information</span></span>



| <span data-ttu-id="d1fdb-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="d1fdb-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="d1fdb-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d1fdb-113">Element Type</span></span> <br/>   | <span data-ttu-id="d1fdb-114">Característica</span><span class="sxs-lookup"><span data-stu-id="d1fdb-114">Feature</span></span><br/> |
| <span data-ttu-id="d1fdb-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d1fdb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d1fdb-116">Página</span><span class="sxs-lookup"><span data-stu-id="d1fdb-116">Page</span></span><br/>    |
| <span data-ttu-id="d1fdb-117">Notas</span><span class="sxs-lookup"><span data-stu-id="d1fdb-117">Notes</span></span> <br/>          | <span data-ttu-id="d1fdb-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d1fdb-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d1fdb-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d1fdb-119">Structural Content</span></span>

<span data-ttu-id="d1fdb-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d1fdb-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="d1fdb-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="d1fdb-121">Structure Variables</span></span>

<span data-ttu-id="d1fdb-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d1fdb-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d1fdb-123">Name</span></span>                                   | <span data-ttu-id="d1fdb-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d1fdb-124">Data type</span></span>          | <span data-ttu-id="d1fdb-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="d1fdb-125">Unit</span></span>                      | <span data-ttu-id="d1fdb-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="d1fdb-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d1fdb-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="d1fdb-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fdb-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d1fdb-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="d1fdb-129">string</span><span class="sxs-lookup"><span data-stu-id="d1fdb-129">string</span></span><br/>  | <span data-ttu-id="d1fdb-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="d1fdb-130">characters</span></span><br/>     | <span data-ttu-id="d1fdb-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d1fdb-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d1fdb-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d1fdb-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="d1fdb-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d1fdb-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="d1fdb-135">string</span><span class="sxs-lookup"><span data-stu-id="d1fdb-135">string</span></span><br/>  | <span data-ttu-id="d1fdb-136">N/D</span><span class="sxs-lookup"><span data-stu-id="d1fdb-136">n/a</span></span><br/>            | <span data-ttu-id="d1fdb-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d1fdb-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="d1fdb-139">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="d1fdb-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="d1fdb-140">integer</span><span class="sxs-lookup"><span data-stu-id="d1fdb-140">integer</span></span><br/> | <span data-ttu-id="d1fdb-141">bits por píxel</span><span class="sxs-lookup"><span data-stu-id="d1fdb-141">bits per pixel</span></span><br/> | <span data-ttu-id="d1fdb-142">Mayor que 0, menor que el valor máximo de compatibilidad de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="d1fdb-143">Valor numérico que indica el número de bits por píxel de datos de color admitidos por la impresora.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="d1fdb-144">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="d1fdb-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="d1fdb-145">integer</span><span class="sxs-lookup"><span data-stu-id="d1fdb-145">integer</span></span><br/> | <span data-ttu-id="d1fdb-146">bits por píxel</span><span class="sxs-lookup"><span data-stu-id="d1fdb-146">bits per pixel</span></span><br/> | <span data-ttu-id="d1fdb-147">Mayor que 0, menor que el valor máximo de compatibilidad de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="d1fdb-148">Valor numérico que indica el número de bits por píxel que el controlador principal debe utilizar para su búfer de representación de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d1fdb-149">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="d1fdb-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d1fdb-150">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d1fdb-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d1fdb-151">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="d1fdb-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d1fdb-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1fdb-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1fdb-153">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d1fdb-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




