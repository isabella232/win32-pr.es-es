---
description: Obtenga información sobre el elemento JobNUpAllDocumentsContiguously, que describe la salida de varias páginas lógicas en una sola hoja física.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408868"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="49276-103">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="49276-103">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="49276-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="49276-104">This topic is not current.</span></span> <span data-ttu-id="49276-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49276-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49276-106">Describe la salida de varias páginas lógicas en una sola hoja física.</span><span class="sxs-lookup"><span data-stu-id="49276-106">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="49276-107">Todos los documentos del trabajo se compilan juntos de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="49276-107">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="49276-108">JobNUpAllDocumentsContiguously y DocumentNUp son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="49276-108">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="49276-109">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="49276-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="49276-110">En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene 2 páginas.</span><span class="sxs-lookup"><span data-stu-id="49276-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="49276-111">Cada documento del trabajo se dúplex de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="49276-111">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="49276-112">Las instrucciones de presentación que se muestran en el ejemplo son la opción RightBottom.</span><span class="sxs-lookup"><span data-stu-id="49276-112">The presentation directions shown in the example is the RightBottom option.</span></span>

![un diagrama que muestra cómo se estableciendo las páginas del documento en una sola hoja en función de la configuración de documentnup](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="49276-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="49276-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="49276-115">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="49276-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="49276-116">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="49276-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="49276-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="49276-117">Element Information</span></span>



| <span data-ttu-id="49276-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="49276-118">Name</span></span> | <span data-ttu-id="49276-119">Valor</span><span class="sxs-lookup"><span data-stu-id="49276-119">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49276-120">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="49276-120">Element Type</span></span> <br/>   | <span data-ttu-id="49276-121">Característica</span><span class="sxs-lookup"><span data-stu-id="49276-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="49276-122">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="49276-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="49276-123">Trabajo</span><span class="sxs-lookup"><span data-stu-id="49276-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="49276-124">Notas</span><span class="sxs-lookup"><span data-stu-id="49276-124">Notes</span></span> <br/>          | <span data-ttu-id="49276-125">Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica mediante el origen del alto y el ancho.</span><span class="sxs-lookup"><span data-stu-id="49276-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="49276-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="49276-126">Structural Content</span></span>

<span data-ttu-id="49276-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="49276-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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

## <a name="structure-variables"></a><span data-ttu-id="49276-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="49276-128">Structure Variables</span></span>

<span data-ttu-id="49276-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="49276-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="49276-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="49276-130">Name</span></span>                                           | <span data-ttu-id="49276-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="49276-131">Data type</span></span>          | <span data-ttu-id="49276-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="49276-132">Unit</span></span>                     | <span data-ttu-id="49276-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="49276-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="49276-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="49276-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49276-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="49276-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="49276-136">string</span><span class="sxs-lookup"><span data-stu-id="49276-136">string</span></span><br/>  | <span data-ttu-id="49276-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="49276-137">characters</span></span><br/>    | <span data-ttu-id="49276-138">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="49276-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="49276-139">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="49276-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="49276-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="49276-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="49276-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="49276-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="49276-142">string</span><span class="sxs-lookup"><span data-stu-id="49276-142">string</span></span><br/>  | <span data-ttu-id="49276-143">N/D</span><span class="sxs-lookup"><span data-stu-id="49276-143">n/a</span></span><br/>           | <span data-ttu-id="49276-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="49276-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="49276-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="49276-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="49276-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="49276-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="49276-147">integer</span><span class="sxs-lookup"><span data-stu-id="49276-147">integer</span></span><br/> | <span data-ttu-id="49276-148">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="49276-148">Logical pages</span></span><br/> | <span data-ttu-id="49276-149">Todos los enteros (mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="49276-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="49276-150">Especifica el número de páginas lógicas por hoja física.</span><span class="sxs-lookup"><span data-stu-id="49276-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="49276-151">El conjunto admitido puede ser cualquier conjunto de enteros, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="49276-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="49276-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="49276-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="49276-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="49276-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="49276-154">string</span><span class="sxs-lookup"><span data-stu-id="49276-154">string</span></span><br/>  | <span data-ttu-id="49276-155">caracteres</span><span class="sxs-lookup"><span data-stu-id="49276-155">characters</span></span><br/>    | <span data-ttu-id="49276-156">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="49276-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="49276-157">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="49276-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="49276-158">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="49276-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="49276-159">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="49276-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="49276-160">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="49276-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="49276-161">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="49276-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="49276-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49276-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49276-163">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="49276-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




