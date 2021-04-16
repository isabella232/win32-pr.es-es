---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b0067e737168bc70b712eaf16ce712446510923
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105649337"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="0c07f-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="0c07f-104">JobBindAllDocuments</span></span>

<span data-ttu-id="0c07f-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="0c07f-105">This topic is not current.</span></span> <span data-ttu-id="0c07f-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0c07f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c07f-107">Describe el método de enlace.</span><span class="sxs-lookup"><span data-stu-id="0c07f-107">Describes the method of binding.</span></span> <span data-ttu-id="0c07f-108">Todos los documentos del trabajo están enlazados juntos.</span><span class="sxs-lookup"><span data-stu-id="0c07f-108">All documents in the job are bound together.</span></span> <span data-ttu-id="0c07f-109">JobBindAllDocuments y DocumentBinding se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="0c07f-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="0c07f-110">Es el controlador el que determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="0c07f-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="0c07f-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0c07f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c07f-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0c07f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0c07f-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="0c07f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0c07f-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0c07f-114">Element Information</span></span>



| <span data-ttu-id="0c07f-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c07f-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0c07f-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0c07f-116">Element Type</span></span> <br/>   | <span data-ttu-id="0c07f-117">Característica</span><span class="sxs-lookup"><span data-stu-id="0c07f-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="0c07f-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="0c07f-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c07f-119">Trabajo</span><span class="sxs-lookup"><span data-stu-id="0c07f-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="0c07f-120">Notas</span><span class="sxs-lookup"><span data-stu-id="0c07f-120">Notes</span></span> <br/>          | <span data-ttu-id="0c07f-121">Top, Bottom, left y right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="0c07f-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0c07f-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0c07f-122">Structural Content</span></span>

<span data-ttu-id="0c07f-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="0c07f-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0c07f-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="0c07f-124">Structure Variables</span></span>

<span data-ttu-id="0c07f-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="0c07f-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c07f-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c07f-126">Name</span></span>                               | <span data-ttu-id="0c07f-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c07f-127">Data type</span></span>          | <span data-ttu-id="0c07f-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="0c07f-128">Unit</span></span>                  | <span data-ttu-id="0c07f-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="0c07f-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0c07f-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="0c07f-130">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c07f-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0c07f-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0c07f-132">string</span><span class="sxs-lookup"><span data-stu-id="0c07f-132">string</span></span><br/>  | <span data-ttu-id="0c07f-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="0c07f-133">characters</span></span><br/> | <span data-ttu-id="0c07f-134">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0c07f-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0c07f-135">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0c07f-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0c07f-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="0c07f-136">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="0c07f-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0c07f-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0c07f-138">string</span><span class="sxs-lookup"><span data-stu-id="0c07f-138">string</span></span><br/>  | <span data-ttu-id="0c07f-139">N/D</span><span class="sxs-lookup"><span data-stu-id="0c07f-139">n/a</span></span><br/>        | <span data-ttu-id="0c07f-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="0c07f-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0c07f-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="0c07f-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="0c07f-142">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="0c07f-142">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="0c07f-143">integer</span><span class="sxs-lookup"><span data-stu-id="0c07f-143">integer</span></span><br/> | <span data-ttu-id="0c07f-144">microns</span><span class="sxs-lookup"><span data-stu-id="0c07f-144">microns</span></span><br/>    | <span data-ttu-id="0c07f-145">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="0c07f-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0c07f-146">Define el margen de enlace mínimo para el enlace de finalización especificado.</span><span class="sxs-lookup"><span data-stu-id="0c07f-146">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="0c07f-147">El medianil se mide en micras en relación con el borde de la dimensión de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="0c07f-147">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0c07f-148">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="0c07f-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0c07f-149">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0c07f-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0c07f-150">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="0c07f-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0c07f-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c07f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c07f-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0c07f-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




