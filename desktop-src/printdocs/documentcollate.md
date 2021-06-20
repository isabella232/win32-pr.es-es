---
description: Obtenga información sobre el elemento DocumentCollate, que describe las características de intercalación de la salida.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409458"
---
# <a name="documentcollate"></a><span data-ttu-id="29b7e-103">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="29b7e-103">DocumentCollate</span></span>

<span data-ttu-id="29b7e-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="29b7e-104">This topic is not current.</span></span> <span data-ttu-id="29b7e-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="29b7e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="29b7e-106">Describe las características de intercalación de la salida.</span><span class="sxs-lookup"><span data-stu-id="29b7e-106">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="29b7e-107">Se intercalan todas las páginas de cada documento individual.</span><span class="sxs-lookup"><span data-stu-id="29b7e-107">All pages in each individual document are collated.</span></span> <span data-ttu-id="29b7e-108">DocumentCollate y JobCollateAlldocuments son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="29b7e-108">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="29b7e-109">El comportamiento y la implementación de si se implementan ambas o solo una de estas palabras clave se deja al controlador.</span><span class="sxs-lookup"><span data-stu-id="29b7e-109">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="29b7e-110">A continuación se deberán seguir las reglas para la implementación de Collate.</span><span class="sxs-lookup"><span data-stu-id="29b7e-110">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="29b7e-111">Definición y reglas de elementos</span><span class="sxs-lookup"><span data-stu-id="29b7e-111">Element Definition and Rules</span></span>

<span data-ttu-id="29b7e-112">Primero debe seguir las reglas de JobCollateAllDocument y, a continuación, aplicar las reglas de DocumentCollate para que los escenarios funcionen.</span><span class="sxs-lookup"><span data-stu-id="29b7e-112">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="29b7e-113">Tenga en cuenta que en un valor de conversión PrintTicket a Devmode, donde JobCollateAllDocuments no es compatible con el controlador, es el controlador el que elige el comportamiento adecuado que se debe tomar (JobCollateAllDocuments = ON u OFF).</span><span class="sxs-lookup"><span data-stu-id="29b7e-113">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="29b7e-114">Además, la opción se puede cambiar en función de otras opciones de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="29b7e-114">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="29b7e-115">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="29b7e-115">JobCollateAllDocuments</span></span>

<span data-ttu-id="29b7e-116">ON: imprima (DocumentCopiesAllPages) copias de cada documento, repita JobCopiesAllDocuments veces.</span><span class="sxs-lookup"><span data-stu-id="29b7e-116">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="29b7e-117">OFF: para cada documento, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntos.</span><span class="sxs-lookup"><span data-stu-id="29b7e-117">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="29b7e-118">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="29b7e-118">DocumentCollate</span></span>

<span data-ttu-id="29b7e-119">ON: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de un documento impreso de forma contigua, intercala las hojas de ese documento.</span><span class="sxs-lookup"><span data-stu-id="29b7e-119">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="29b7e-120">OFF: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) impresas de forma contigua, imprima todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada hoja juntas.</span><span class="sxs-lookup"><span data-stu-id="29b7e-120">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="29b7e-121">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="29b7e-121">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="29b7e-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="29b7e-122">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="29b7e-123">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="29b7e-123">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="29b7e-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="29b7e-124">Element Information</span></span>



| <span data-ttu-id="29b7e-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="29b7e-125">Name</span></span> | <span data-ttu-id="29b7e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="29b7e-126">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="29b7e-127">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="29b7e-127">Element Type</span></span> <br/>   | <span data-ttu-id="29b7e-128">Característica</span><span class="sxs-lookup"><span data-stu-id="29b7e-128">Feature</span></span><br/>  |
| <span data-ttu-id="29b7e-129">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="29b7e-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="29b7e-130">Documento</span><span class="sxs-lookup"><span data-stu-id="29b7e-130">Document</span></span><br/> |
| <span data-ttu-id="29b7e-131">Notas</span><span class="sxs-lookup"><span data-stu-id="29b7e-131">Notes</span></span> <br/>          | <span data-ttu-id="29b7e-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="29b7e-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="29b7e-133">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="29b7e-133">Structural Content</span></span>

<span data-ttu-id="29b7e-134">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="29b7e-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="29b7e-135">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="29b7e-135">Structure Variables</span></span>

<span data-ttu-id="29b7e-136">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="29b7e-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="29b7e-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="29b7e-137">Name</span></span>                               | <span data-ttu-id="29b7e-138">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="29b7e-138">Data type</span></span>         | <span data-ttu-id="29b7e-139">Unidad</span><span class="sxs-lookup"><span data-stu-id="29b7e-139">Unit</span></span>                  | <span data-ttu-id="29b7e-140">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="29b7e-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="29b7e-141">Resumen</span><span class="sxs-lookup"><span data-stu-id="29b7e-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="29b7e-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="29b7e-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="29b7e-143">string</span><span class="sxs-lookup"><span data-stu-id="29b7e-143">string</span></span><br/> | <span data-ttu-id="29b7e-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="29b7e-144">characters</span></span><br/> | <span data-ttu-id="29b7e-145">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="29b7e-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="29b7e-146">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="29b7e-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="29b7e-147">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="29b7e-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="29b7e-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="29b7e-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="29b7e-149">string</span><span class="sxs-lookup"><span data-stu-id="29b7e-149">string</span></span><br/> | <span data-ttu-id="29b7e-150">N/D</span><span class="sxs-lookup"><span data-stu-id="29b7e-150">n/a</span></span><br/>        | <span data-ttu-id="29b7e-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="29b7e-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="29b7e-152">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="29b7e-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="29b7e-153">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="29b7e-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="29b7e-154">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="29b7e-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="29b7e-155">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="29b7e-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="29b7e-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29b7e-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29b7e-157">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="29b7e-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




