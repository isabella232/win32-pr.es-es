---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f90620ac99bf97e85acb22c723a938c31605bd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998092"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="a6d36-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="a6d36-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="a6d36-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="a6d36-105">This topic is not current.</span></span> <span data-ttu-id="a6d36-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a6d36-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a6d36-107">Describe la salida de varias páginas lógicas en una sola hoja física.</span><span class="sxs-lookup"><span data-stu-id="a6d36-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="a6d36-108">Todos los documentos del trabajo se compilan juntos de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="a6d36-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="a6d36-109">JobNUpAllDocumentsContiguously y DocumentNUp son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="a6d36-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="a6d36-110">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="a6d36-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="a6d36-111">En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene 2 páginas.</span><span class="sxs-lookup"><span data-stu-id="a6d36-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="a6d36-112">Cada documento del trabajo se dúplex de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="a6d36-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="a6d36-113">Las direcciones de presentación que se muestran en el ejemplo son la opción RightBottom.</span><span class="sxs-lookup"><span data-stu-id="a6d36-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![diagrama que muestra cómo se estableciendo las páginas del documento en una sola hoja en función de la configuración de documentnup](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="a6d36-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a6d36-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a6d36-116">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="a6d36-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a6d36-117">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a6d36-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a6d36-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a6d36-118">Element Information</span></span>



| <span data-ttu-id="a6d36-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6d36-119">Name</span></span> | <span data-ttu-id="a6d36-120">Value</span><span class="sxs-lookup"><span data-stu-id="a6d36-120">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d36-121">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a6d36-121">Element Type</span></span> <br/>   | <span data-ttu-id="a6d36-122">Característica</span><span class="sxs-lookup"><span data-stu-id="a6d36-122">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="a6d36-123">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="a6d36-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a6d36-124">Trabajo</span><span class="sxs-lookup"><span data-stu-id="a6d36-124">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="a6d36-125">Notas</span><span class="sxs-lookup"><span data-stu-id="a6d36-125">Notes</span></span> <br/>          | <span data-ttu-id="a6d36-126">Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica por el origen del alto y el ancho.</span><span class="sxs-lookup"><span data-stu-id="a6d36-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a6d36-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="a6d36-127">Structural Content</span></span>

<span data-ttu-id="a6d36-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="a6d36-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a6d36-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="a6d36-129">Structure Variables</span></span>

<span data-ttu-id="a6d36-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="a6d36-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a6d36-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6d36-131">Name</span></span>                                           | <span data-ttu-id="a6d36-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a6d36-132">Data type</span></span>          | <span data-ttu-id="a6d36-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="a6d36-133">Unit</span></span>                     | <span data-ttu-id="a6d36-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="a6d36-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a6d36-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="a6d36-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d36-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a6d36-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="a6d36-137">string</span><span class="sxs-lookup"><span data-stu-id="a6d36-137">string</span></span><br/>  | <span data-ttu-id="a6d36-138">caracteres</span><span class="sxs-lookup"><span data-stu-id="a6d36-138">characters</span></span><br/>    | <span data-ttu-id="a6d36-139">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a6d36-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a6d36-140">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6d36-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a6d36-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="a6d36-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="a6d36-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a6d36-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="a6d36-143">string</span><span class="sxs-lookup"><span data-stu-id="a6d36-143">string</span></span><br/>  | <span data-ttu-id="a6d36-144">N/D</span><span class="sxs-lookup"><span data-stu-id="a6d36-144">n/a</span></span><br/>           | <span data-ttu-id="a6d36-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="a6d36-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a6d36-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="a6d36-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="a6d36-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="a6d36-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="a6d36-148">integer</span><span class="sxs-lookup"><span data-stu-id="a6d36-148">integer</span></span><br/> | <span data-ttu-id="a6d36-149">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="a6d36-149">Logical pages</span></span><br/> | <span data-ttu-id="a6d36-150">Todos los enteros (mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="a6d36-150">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="a6d36-151">Especifica el número de páginas lógicas por hoja física.</span><span class="sxs-lookup"><span data-stu-id="a6d36-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="a6d36-152">El conjunto admitido puede ser cualquier conjunto de enteros, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a6d36-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="a6d36-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="a6d36-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="a6d36-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="a6d36-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="a6d36-155">string</span><span class="sxs-lookup"><span data-stu-id="a6d36-155">string</span></span><br/>  | <span data-ttu-id="a6d36-156">caracteres</span><span class="sxs-lookup"><span data-stu-id="a6d36-156">characters</span></span><br/>    | <span data-ttu-id="a6d36-157">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a6d36-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a6d36-158">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6d36-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a6d36-159">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="a6d36-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a6d36-160">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a6d36-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a6d36-161">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="a6d36-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a6d36-162">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="a6d36-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a6d36-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6d36-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d36-164">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="a6d36-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




