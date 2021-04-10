---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279913"
---
# <a name="documentnup"></a><span data-ttu-id="ceb84-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="ceb84-104">DocumentNUp</span></span>

<span data-ttu-id="ceb84-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="ceb84-105">This topic is not current.</span></span> <span data-ttu-id="ceb84-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ceb84-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ceb84-107">Describe la salida y el formato de varias páginas lógicas en una sola hoja física.</span><span class="sxs-lookup"><span data-stu-id="ceb84-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="ceb84-108">Cada documento se compila por separado.</span><span class="sxs-lookup"><span data-stu-id="ceb84-108">Each document is compiled separately.</span></span> <span data-ttu-id="ceb84-109">DocumentNUp y JobNUpAllDocumentsContiguously se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="ceb84-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="ceb84-110">Es el controlador el que determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="ceb84-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="ceb84-111">En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene dos páginas.</span><span class="sxs-lookup"><span data-stu-id="ceb84-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="ceb84-112">Cada documento está dúplex por separado.</span><span class="sxs-lookup"><span data-stu-id="ceb84-112">Each document is duplexed separately.</span></span> <span data-ttu-id="ceb84-113">La dirección de presentación que se muestra a continuación es la opción RightBottom.</span><span class="sxs-lookup"><span data-stu-id="ceb84-113">The presentation direction shown below is the RightBottom option.</span></span>

![diagrama que muestra cómo se colocan las páginas del documento en una sola hoja basada en la configuración de documentnup](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="ceb84-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ceb84-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ceb84-116">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ceb84-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ceb84-117">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="ceb84-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ceb84-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ceb84-118">Element Information</span></span>



| <span data-ttu-id="ceb84-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceb84-119">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb84-120">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ceb84-120">Element Type</span></span> <br/>   | <span data-ttu-id="ceb84-121">Característica</span><span class="sxs-lookup"><span data-stu-id="ceb84-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ceb84-122">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ceb84-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ceb84-123">Documento</span><span class="sxs-lookup"><span data-stu-id="ceb84-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="ceb84-124">Notas</span><span class="sxs-lookup"><span data-stu-id="ceb84-124">Notes</span></span> <br/>          | <span data-ttu-id="ceb84-125">Los valores superior, inferior, izquierdo y derecho son relativos a la PageImageableSize, donde el origen de los ejes x e y indica que el lado izquierdo lo denota.</span><span class="sxs-lookup"><span data-stu-id="ceb84-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ceb84-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ceb84-126">Structural Content</span></span>

<span data-ttu-id="ceb84-127">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ceb84-127">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ceb84-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="ceb84-128">Structure Variables</span></span>

<span data-ttu-id="ceb84-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ceb84-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ceb84-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceb84-130">Name</span></span>                                           | <span data-ttu-id="ceb84-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ceb84-131">Data type</span></span>          | <span data-ttu-id="ceb84-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="ceb84-132">Unit</span></span>                     | <span data-ttu-id="ceb84-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="ceb84-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ceb84-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="ceb84-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb84-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ceb84-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="ceb84-136">string</span><span class="sxs-lookup"><span data-stu-id="ceb84-136">string</span></span><br/>  | <span data-ttu-id="ceb84-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="ceb84-137">characters</span></span><br/>    | <span data-ttu-id="ceb84-138">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ceb84-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ceb84-139">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ceb84-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ceb84-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="ceb84-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="ceb84-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ceb84-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="ceb84-142">string</span><span class="sxs-lookup"><span data-stu-id="ceb84-142">string</span></span><br/>  | <span data-ttu-id="ceb84-143">N/D</span><span class="sxs-lookup"><span data-stu-id="ceb84-143">n/a</span></span><br/>           | <span data-ttu-id="ceb84-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="ceb84-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ceb84-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="ceb84-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="ceb84-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="ceb84-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="ceb84-147">integer</span><span class="sxs-lookup"><span data-stu-id="ceb84-147">integer</span></span><br/> | <span data-ttu-id="ceb84-148">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="ceb84-148">Logical pages</span></span><br/> | <span data-ttu-id="ceb84-149">Todos los enteros (mayores que cero).</span><span class="sxs-lookup"><span data-stu-id="ceb84-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="ceb84-150">Especifica el número de páginas lógicas por hoja física.</span><span class="sxs-lookup"><span data-stu-id="ceb84-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="ceb84-151">El conjunto compatible puede ser cualquier conjunto de enteros, por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="ceb84-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="ceb84-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="ceb84-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="ceb84-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="ceb84-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="ceb84-154">string</span><span class="sxs-lookup"><span data-stu-id="ceb84-154">string</span></span><br/>  | <span data-ttu-id="ceb84-155">caracteres</span><span class="sxs-lookup"><span data-stu-id="ceb84-155">characters</span></span><br/>    | <span data-ttu-id="ceb84-156">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ceb84-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ceb84-157">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ceb84-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ceb84-158">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="ceb84-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ceb84-159">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="ceb84-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ceb84-160">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="ceb84-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ceb84-161">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="ceb84-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ceb84-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ceb84-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceb84-163">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ceb84-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




