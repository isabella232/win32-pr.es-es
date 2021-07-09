---
description: Obtenga información sobre el elemento PageOutputColor configurable por el usuario. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548993"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="9d77d-105">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="9d77d-105">PageOutputColor</span></span>

<span data-ttu-id="9d77d-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9d77d-106">This topic is not current.</span></span> <span data-ttu-id="9d77d-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9d77d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d77d-108">Describe las características de la configuración de color para la salida.</span><span class="sxs-lookup"><span data-stu-id="9d77d-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="9d77d-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9d77d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9d77d-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9d77d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9d77d-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9d77d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9d77d-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9d77d-112">Element Information</span></span>



| <span data-ttu-id="9d77d-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d77d-113">Name</span></span> | <span data-ttu-id="9d77d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9d77d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9d77d-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9d77d-115">Element Type</span></span> <br/>   | <span data-ttu-id="9d77d-116">Característica</span><span class="sxs-lookup"><span data-stu-id="9d77d-116">Feature</span></span><br/> |
| <span data-ttu-id="9d77d-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9d77d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9d77d-118">Página</span><span class="sxs-lookup"><span data-stu-id="9d77d-118">Page</span></span><br/>    |
| <span data-ttu-id="9d77d-119">Notas</span><span class="sxs-lookup"><span data-stu-id="9d77d-119">Notes</span></span> <br/>          | <span data-ttu-id="9d77d-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d77d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9d77d-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9d77d-121">Structural Content</span></span>

<span data-ttu-id="9d77d-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9d77d-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9d77d-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9d77d-123">Structure Variables</span></span>

<span data-ttu-id="9d77d-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9d77d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9d77d-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d77d-125">Name</span></span>                                   | <span data-ttu-id="9d77d-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9d77d-126">Data type</span></span>          | <span data-ttu-id="9d77d-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="9d77d-127">Unit</span></span>                      | <span data-ttu-id="9d77d-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9d77d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9d77d-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="9d77d-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d77d-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9d77d-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9d77d-131">string</span><span class="sxs-lookup"><span data-stu-id="9d77d-131">string</span></span><br/>  | <span data-ttu-id="9d77d-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="9d77d-132">characters</span></span><br/>     | <span data-ttu-id="9d77d-133">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9d77d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9d77d-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9d77d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9d77d-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9d77d-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="9d77d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9d77d-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9d77d-137">string</span><span class="sxs-lookup"><span data-stu-id="9d77d-137">string</span></span><br/>  | <span data-ttu-id="9d77d-138">N/D</span><span class="sxs-lookup"><span data-stu-id="9d77d-138">n/a</span></span><br/>            | <span data-ttu-id="9d77d-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="9d77d-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9d77d-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9d77d-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="9d77d-141">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="9d77d-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="9d77d-142">integer</span><span class="sxs-lookup"><span data-stu-id="9d77d-142">integer</span></span><br/> | <span data-ttu-id="9d77d-143">bits por píxel</span><span class="sxs-lookup"><span data-stu-id="9d77d-143">bits per pixel</span></span><br/> | <span data-ttu-id="9d77d-144">Mayor que 0, menor que el valor máximo de compatibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d77d-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="9d77d-145">Valor numérico que indica el número de bits por píxel de datos de color admitidos por la impresora.</span><span class="sxs-lookup"><span data-stu-id="9d77d-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="9d77d-146">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="9d77d-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="9d77d-147">integer</span><span class="sxs-lookup"><span data-stu-id="9d77d-147">integer</span></span><br/> | <span data-ttu-id="9d77d-148">bits por píxel</span><span class="sxs-lookup"><span data-stu-id="9d77d-148">bits per pixel</span></span><br/> | <span data-ttu-id="9d77d-149">Mayor que 0, menor que el valor máximo de compatibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d77d-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="9d77d-150">Valor numérico que indica el número de bits por píxel que el controlador principal debe usar para su búfer de representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="9d77d-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9d77d-151">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9d77d-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9d77d-152">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9d77d-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9d77d-153">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9d77d-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9d77d-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d77d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d77d-155">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9d77d-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




