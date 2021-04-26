---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab531a2095e83aa35f3dff450270c2a5b4520d62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996292"
---
# <a name="documentnup"></a><span data-ttu-id="1baea-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="1baea-104">DocumentNUp</span></span>

<span data-ttu-id="1baea-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1baea-105">This topic is not current.</span></span> <span data-ttu-id="1baea-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1baea-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1baea-107">Describe la salida y el formato de varias páginas lógicas en una sola hoja física.</span><span class="sxs-lookup"><span data-stu-id="1baea-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="1baea-108">Cada documento se compila por separado.</span><span class="sxs-lookup"><span data-stu-id="1baea-108">Each document is compiled separately.</span></span> <span data-ttu-id="1baea-109">DocumentNUp y JobNUpAllDocumentsContiguously son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="1baea-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="1baea-110">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="1baea-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="1baea-111">En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene 2 páginas.</span><span class="sxs-lookup"><span data-stu-id="1baea-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="1baea-112">Cada documento se dúplex por separado.</span><span class="sxs-lookup"><span data-stu-id="1baea-112">Each document is duplexed separately.</span></span> <span data-ttu-id="1baea-113">La dirección de presentación que se muestra a continuación es la opción RightBottom.</span><span class="sxs-lookup"><span data-stu-id="1baea-113">The presentation direction shown below is the RightBottom option.</span></span>

![diagrama que muestra cómo se estableciendo las páginas del documento en una sola hoja en función de la configuración de documentnup](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="1baea-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1baea-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1baea-116">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1baea-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1baea-117">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1baea-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1baea-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1baea-118">Element Information</span></span>



| <span data-ttu-id="1baea-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="1baea-119">Name</span></span> | <span data-ttu-id="1baea-120">Value</span><span class="sxs-lookup"><span data-stu-id="1baea-120">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1baea-121">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1baea-121">Element Type</span></span> <br/>   | <span data-ttu-id="1baea-122">Característica</span><span class="sxs-lookup"><span data-stu-id="1baea-122">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="1baea-123">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1baea-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1baea-124">Documento</span><span class="sxs-lookup"><span data-stu-id="1baea-124">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="1baea-125">Notas</span><span class="sxs-lookup"><span data-stu-id="1baea-125">Notes</span></span> <br/>          | <span data-ttu-id="1baea-126">Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica mediante el origen del eje X y el eje Y.</span><span class="sxs-lookup"><span data-stu-id="1baea-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1baea-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1baea-127">Structural Content</span></span>

<span data-ttu-id="1baea-128">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="1baea-128">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="1baea-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="1baea-129">Structure Variables</span></span>

<span data-ttu-id="1baea-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1baea-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1baea-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="1baea-131">Name</span></span>                                           | <span data-ttu-id="1baea-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1baea-132">Data type</span></span>          | <span data-ttu-id="1baea-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="1baea-133">Unit</span></span>                     | <span data-ttu-id="1baea-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="1baea-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1baea-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="1baea-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1baea-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1baea-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="1baea-137">string</span><span class="sxs-lookup"><span data-stu-id="1baea-137">string</span></span><br/>  | <span data-ttu-id="1baea-138">caracteres</span><span class="sxs-lookup"><span data-stu-id="1baea-138">characters</span></span><br/>    | <span data-ttu-id="1baea-139">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1baea-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1baea-140">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1baea-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1baea-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1baea-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="1baea-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1baea-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="1baea-143">string</span><span class="sxs-lookup"><span data-stu-id="1baea-143">string</span></span><br/>  | <span data-ttu-id="1baea-144">N/D</span><span class="sxs-lookup"><span data-stu-id="1baea-144">n/a</span></span><br/>           | <span data-ttu-id="1baea-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="1baea-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1baea-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1baea-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="1baea-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="1baea-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="1baea-148">integer</span><span class="sxs-lookup"><span data-stu-id="1baea-148">integer</span></span><br/> | <span data-ttu-id="1baea-149">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="1baea-149">Logical pages</span></span><br/> | <span data-ttu-id="1baea-150">Todos los enteros (mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="1baea-150">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="1baea-151">Especifica el número de páginas lógicas por hoja física.</span><span class="sxs-lookup"><span data-stu-id="1baea-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="1baea-152">El conjunto admitido puede ser cualquier conjunto de enteros, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1baea-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="1baea-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="1baea-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="1baea-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="1baea-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="1baea-155">string</span><span class="sxs-lookup"><span data-stu-id="1baea-155">string</span></span><br/>  | <span data-ttu-id="1baea-156">caracteres</span><span class="sxs-lookup"><span data-stu-id="1baea-156">characters</span></span><br/>    | <span data-ttu-id="1baea-157">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1baea-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1baea-158">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1baea-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1baea-159">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1baea-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1baea-160">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1baea-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1baea-161">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="1baea-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1baea-162">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="1baea-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="1baea-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1baea-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1baea-164">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1baea-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




