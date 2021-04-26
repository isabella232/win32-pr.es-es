---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: DocumentBinding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4aeb31acb72932bbf272d52676b7795abe8311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996302"
---
# <a name="documentbinding"></a><span data-ttu-id="239db-104">DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="239db-104">DocumentBinding</span></span>

<span data-ttu-id="239db-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="239db-105">This topic is not current.</span></span> <span data-ttu-id="239db-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="239db-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="239db-107">Describe el método de enlace.</span><span class="sxs-lookup"><span data-stu-id="239db-107">Describes the method of binding.</span></span> <span data-ttu-id="239db-108">Cada documento se enlaza por separado.</span><span class="sxs-lookup"><span data-stu-id="239db-108">Each document is bound separately.</span></span> <span data-ttu-id="239db-109">DocumentBinding y JobBindAllDocuments son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="239db-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="239db-110">Es el controlador quien determina el control de restricciones entre palabras clave.</span><span class="sxs-lookup"><span data-stu-id="239db-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="239db-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="239db-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="239db-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="239db-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="239db-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="239db-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="239db-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="239db-114">Element Information</span></span>



| <span data-ttu-id="239db-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="239db-115">Name</span></span> | <span data-ttu-id="239db-116">Value</span><span class="sxs-lookup"><span data-stu-id="239db-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239db-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="239db-117">Element Type</span></span> <br/>   | <span data-ttu-id="239db-118">Característica</span><span class="sxs-lookup"><span data-stu-id="239db-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="239db-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="239db-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="239db-120">Documento</span><span class="sxs-lookup"><span data-stu-id="239db-120">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="239db-121">Notas</span><span class="sxs-lookup"><span data-stu-id="239db-121">Notes</span></span> <br/>          | <span data-ttu-id="239db-122">Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica mediante el origen del eje X y el eje Y.</span><span class="sxs-lookup"><span data-stu-id="239db-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="239db-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="239db-123">Structural Content</span></span>

<span data-ttu-id="239db-124">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="239db-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="239db-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="239db-125">Structure Variables</span></span>

<span data-ttu-id="239db-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="239db-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="239db-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="239db-127">Name</span></span>                               | <span data-ttu-id="239db-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="239db-128">Data type</span></span>          | <span data-ttu-id="239db-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="239db-129">Unit</span></span>                  | <span data-ttu-id="239db-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="239db-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="239db-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="239db-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239db-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="239db-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="239db-133">string</span><span class="sxs-lookup"><span data-stu-id="239db-133">string</span></span><br/>  | <span data-ttu-id="239db-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="239db-134">characters</span></span><br/> | <span data-ttu-id="239db-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="239db-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="239db-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="239db-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="239db-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="239db-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="239db-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="239db-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="239db-139">string</span><span class="sxs-lookup"><span data-stu-id="239db-139">string</span></span><br/>  | <span data-ttu-id="239db-140">N/D</span><span class="sxs-lookup"><span data-stu-id="239db-140">n/a</span></span><br/>        | <span data-ttu-id="239db-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="239db-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="239db-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="239db-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="239db-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="239db-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="239db-144">Entero</span><span class="sxs-lookup"><span data-stu-id="239db-144">Integer</span></span><br/> | <span data-ttu-id="239db-145">Micras</span><span class="sxs-lookup"><span data-stu-id="239db-145">microns</span></span><br/>    | <span data-ttu-id="239db-146">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="239db-146">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="239db-147">Define el median de enlace mínimo para el enlace final especificado.</span><span class="sxs-lookup"><span data-stu-id="239db-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="239db-148">El medianía se mide en micrones con respecto al borde de la dimensión de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="239db-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="239db-149">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="239db-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="239db-150">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="239db-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="239db-151">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="239db-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale" >
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="239db-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="239db-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239db-153">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="239db-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




