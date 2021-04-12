---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e307883a25fc977b9086259789c04f4b3a7cbf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361998"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="1defa-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="1defa-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="1defa-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="1defa-105">This topic is not current.</span></span> <span data-ttu-id="1defa-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1defa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1defa-107">Describe el resultado de varias páginas lógicas en una sola hoja física.</span><span class="sxs-lookup"><span data-stu-id="1defa-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="1defa-108">Todos los documentos del trabajo se compilan de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="1defa-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="1defa-109">JobNUpAllDocumentsContiguously y DocumentNUp se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="1defa-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="1defa-110">Es el controlador el que determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="1defa-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="1defa-111">En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene dos páginas.</span><span class="sxs-lookup"><span data-stu-id="1defa-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="1defa-112">Cada documento del trabajo está en dúplex contiguo.</span><span class="sxs-lookup"><span data-stu-id="1defa-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="1defa-113">Las direcciones de presentación que se muestran en el ejemplo son la opción RightBottom.</span><span class="sxs-lookup"><span data-stu-id="1defa-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![diagrama que muestra cómo se colocan las páginas del documento en una sola hoja basada en la configuración de documentnup](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="1defa-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1defa-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1defa-116">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1defa-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1defa-117">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="1defa-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1defa-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1defa-118">Element Information</span></span>



| <span data-ttu-id="1defa-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="1defa-119">Name</span></span>                       |                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1defa-120">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1defa-120">Element Type</span></span> <br/>   | <span data-ttu-id="1defa-121">Característica</span><span class="sxs-lookup"><span data-stu-id="1defa-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="1defa-122">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1defa-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1defa-123">Trabajo</span><span class="sxs-lookup"><span data-stu-id="1defa-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="1defa-124">Notas</span><span class="sxs-lookup"><span data-stu-id="1defa-124">Notes</span></span> <br/>          | <span data-ttu-id="1defa-125">Los de arriba, abajo, a la izquierda y a la derecha son relativos al PageImageableSize, donde la parte superior se indica mediante el origen del alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="1defa-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1defa-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1defa-126">Structural Content</span></span>

<span data-ttu-id="1defa-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="1defa-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1defa-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="1defa-128">Structure Variables</span></span>

<span data-ttu-id="1defa-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1defa-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1defa-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="1defa-130">Name</span></span>                                           | <span data-ttu-id="1defa-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1defa-131">Data type</span></span>          | <span data-ttu-id="1defa-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="1defa-132">Unit</span></span>                     | <span data-ttu-id="1defa-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="1defa-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1defa-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="1defa-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1defa-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1defa-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="1defa-136">string</span><span class="sxs-lookup"><span data-stu-id="1defa-136">string</span></span><br/>  | <span data-ttu-id="1defa-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="1defa-137">characters</span></span><br/>    | <span data-ttu-id="1defa-138">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1defa-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1defa-139">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1defa-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1defa-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1defa-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="1defa-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1defa-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="1defa-142">string</span><span class="sxs-lookup"><span data-stu-id="1defa-142">string</span></span><br/>  | <span data-ttu-id="1defa-143">N/D</span><span class="sxs-lookup"><span data-stu-id="1defa-143">n/a</span></span><br/>           | <span data-ttu-id="1defa-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="1defa-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1defa-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1defa-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="1defa-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="1defa-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="1defa-147">integer</span><span class="sxs-lookup"><span data-stu-id="1defa-147">integer</span></span><br/> | <span data-ttu-id="1defa-148">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="1defa-148">Logical pages</span></span><br/> | <span data-ttu-id="1defa-149">Todos los enteros (mayores que cero).</span><span class="sxs-lookup"><span data-stu-id="1defa-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="1defa-150">Especifica el número de páginas lógicas por hoja física.</span><span class="sxs-lookup"><span data-stu-id="1defa-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="1defa-151">El conjunto compatible puede ser cualquier conjunto de enteros, por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="1defa-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="1defa-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="1defa-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="1defa-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="1defa-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="1defa-154">string</span><span class="sxs-lookup"><span data-stu-id="1defa-154">string</span></span><br/>  | <span data-ttu-id="1defa-155">caracteres</span><span class="sxs-lookup"><span data-stu-id="1defa-155">characters</span></span><br/>    | <span data-ttu-id="1defa-156">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1defa-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1defa-157">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1defa-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1defa-158">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1defa-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1defa-159">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="1defa-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1defa-160">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="1defa-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1defa-161">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="1defa-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1defa-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1defa-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1defa-163">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1defa-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




