---
description: Obtenga información sobre el elemento JobBindAllDocuments, que describe el método de enlace. Todos los documentos del trabajo se enlazan juntos.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5abff455756b2abc1d84bf2cff470fa49c93278
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409088"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="bf195-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="bf195-104">JobBindAllDocuments</span></span>

<span data-ttu-id="bf195-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="bf195-105">This topic is not current.</span></span> <span data-ttu-id="bf195-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bf195-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bf195-107">Describe el método de enlace.</span><span class="sxs-lookup"><span data-stu-id="bf195-107">Describes the method of binding.</span></span> <span data-ttu-id="bf195-108">Todos los documentos del trabajo se enlazan juntos.</span><span class="sxs-lookup"><span data-stu-id="bf195-108">All documents in the job are bound together.</span></span> <span data-ttu-id="bf195-109">JobBindAllDocuments y DocumentBinding son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="bf195-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="bf195-110">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="bf195-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="bf195-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bf195-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bf195-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="bf195-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bf195-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bf195-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bf195-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bf195-114">Element Information</span></span>



| <span data-ttu-id="bf195-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf195-115">Name</span></span> | <span data-ttu-id="bf195-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bf195-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bf195-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bf195-117">Element Type</span></span> <br/>   | <span data-ttu-id="bf195-118">Característica</span><span class="sxs-lookup"><span data-stu-id="bf195-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="bf195-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bf195-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bf195-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="bf195-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="bf195-121">Notas</span><span class="sxs-lookup"><span data-stu-id="bf195-121">Notes</span></span> <br/>          | <span data-ttu-id="bf195-122">Top, Bottom, Left y Right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="bf195-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bf195-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="bf195-123">Structural Content</span></span>

<span data-ttu-id="bf195-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="bf195-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="bf195-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="bf195-125">Structure Variables</span></span>

<span data-ttu-id="bf195-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bf195-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bf195-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf195-127">Name</span></span>                               | <span data-ttu-id="bf195-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bf195-128">Data type</span></span>          | <span data-ttu-id="bf195-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="bf195-129">Unit</span></span>                  | <span data-ttu-id="bf195-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="bf195-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bf195-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="bf195-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf195-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="bf195-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bf195-133">string</span><span class="sxs-lookup"><span data-stu-id="bf195-133">string</span></span><br/>  | <span data-ttu-id="bf195-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="bf195-134">characters</span></span><br/> | <span data-ttu-id="bf195-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="bf195-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bf195-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bf195-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bf195-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="bf195-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="bf195-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bf195-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bf195-139">string</span><span class="sxs-lookup"><span data-stu-id="bf195-139">string</span></span><br/>  | <span data-ttu-id="bf195-140">N/D</span><span class="sxs-lookup"><span data-stu-id="bf195-140">n/a</span></span><br/>        | <span data-ttu-id="bf195-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="bf195-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bf195-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="bf195-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="bf195-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="bf195-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="bf195-144">integer</span><span class="sxs-lookup"><span data-stu-id="bf195-144">integer</span></span><br/> | <span data-ttu-id="bf195-145">Micras</span><span class="sxs-lookup"><span data-stu-id="bf195-145">microns</span></span><br/>    | <span data-ttu-id="bf195-146">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="bf195-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="bf195-147">Define el median de enlace mínimo para el enlace final especificado.</span><span class="sxs-lookup"><span data-stu-id="bf195-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="bf195-148">El medianía se mide en micrones en relación con el borde de la dimensión multimedia física.</span><span class="sxs-lookup"><span data-stu-id="bf195-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bf195-149">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bf195-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bf195-150">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="bf195-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bf195-151">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="bf195-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="bf195-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf195-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf195-153">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bf195-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




