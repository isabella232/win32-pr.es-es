---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: DocumentBinding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139cc40701624041a57e4fa69edc084f88c1972b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717442"
---
# <a name="documentbinding"></a><span data-ttu-id="6a110-104">DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="6a110-104">DocumentBinding</span></span>

<span data-ttu-id="6a110-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="6a110-105">This topic is not current.</span></span> <span data-ttu-id="6a110-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6a110-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6a110-107">Describe el método de enlace.</span><span class="sxs-lookup"><span data-stu-id="6a110-107">Describes the method of binding.</span></span> <span data-ttu-id="6a110-108">Cada documento se enlaza por separado.</span><span class="sxs-lookup"><span data-stu-id="6a110-108">Each document is bound separately.</span></span> <span data-ttu-id="6a110-109">DocumentBinding y JobBindAllDocuments se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="6a110-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="6a110-110">Es el controlador el que determina el control de restricciones entre las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="6a110-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="6a110-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6a110-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6a110-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6a110-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6a110-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="6a110-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6a110-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6a110-114">Element Information</span></span>



| <span data-ttu-id="6a110-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="6a110-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a110-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6a110-116">Element Type</span></span> <br/>   | <span data-ttu-id="6a110-117">Característica</span><span class="sxs-lookup"><span data-stu-id="6a110-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="6a110-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="6a110-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6a110-119">Documento</span><span class="sxs-lookup"><span data-stu-id="6a110-119">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="6a110-120">Notas</span><span class="sxs-lookup"><span data-stu-id="6a110-120">Notes</span></span> <br/>          | <span data-ttu-id="6a110-121">Los valores superior, inferior, izquierdo y derecho son relativos a la PageImageableSize, donde el origen de los ejes x e y indica que el lado izquierdo lo denota.</span><span class="sxs-lookup"><span data-stu-id="6a110-121">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6a110-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6a110-122">Structural Content</span></span>

<span data-ttu-id="6a110-123">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a110-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6a110-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="6a110-124">Structure Variables</span></span>

<span data-ttu-id="6a110-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="6a110-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6a110-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="6a110-126">Name</span></span>                               | <span data-ttu-id="6a110-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6a110-127">Data type</span></span>          | <span data-ttu-id="6a110-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="6a110-128">Unit</span></span>                  | <span data-ttu-id="6a110-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="6a110-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6a110-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="6a110-130">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a110-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6a110-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6a110-132">string</span><span class="sxs-lookup"><span data-stu-id="6a110-132">string</span></span><br/>  | <span data-ttu-id="6a110-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="6a110-133">characters</span></span><br/> | <span data-ttu-id="6a110-134">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6a110-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6a110-135">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6a110-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6a110-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="6a110-136">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="6a110-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6a110-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6a110-138">string</span><span class="sxs-lookup"><span data-stu-id="6a110-138">string</span></span><br/>  | <span data-ttu-id="6a110-139">N/D</span><span class="sxs-lookup"><span data-stu-id="6a110-139">n/a</span></span><br/>        | <span data-ttu-id="6a110-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="6a110-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6a110-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="6a110-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="6a110-142">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="6a110-142">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="6a110-143">Entero</span><span class="sxs-lookup"><span data-stu-id="6a110-143">Integer</span></span><br/> | <span data-ttu-id="6a110-144">microns</span><span class="sxs-lookup"><span data-stu-id="6a110-144">microns</span></span><br/>    | <span data-ttu-id="6a110-145">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="6a110-145">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="6a110-146">Define el margen de enlace mínimo para el enlace de finalización especificado.</span><span class="sxs-lookup"><span data-stu-id="6a110-146">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="6a110-147">El medianil se mide en micras en relación con el borde de la dimensión de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="6a110-147">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6a110-148">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="6a110-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6a110-149">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="6a110-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6a110-150">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="6a110-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6a110-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a110-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a110-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6a110-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




