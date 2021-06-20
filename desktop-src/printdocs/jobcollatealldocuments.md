---
description: Obtenga información sobre cómo el elemento JobCollateAllDocuments describe las características de intercalación de la salida. Todos los documentos de cada trabajo individual se intercalan.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75eb21fcd518f0fda4edd4c3c4eff721a6a5b17
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409068"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="def38-104">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="def38-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="def38-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="def38-105">This topic is not current.</span></span> <span data-ttu-id="def38-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="def38-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="def38-107">Describe las características de intercalación de la salida.</span><span class="sxs-lookup"><span data-stu-id="def38-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="def38-108">Todos los documentos de cada trabajo individual se intercalan.</span><span class="sxs-lookup"><span data-stu-id="def38-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="def38-109">DocumentCollate y JobCollateAlldocuments son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="def38-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="def38-110">El comportamiento y la implementación de si se implementan ambas o solo una de estas palabras clave se deja al controlador.</span><span class="sxs-lookup"><span data-stu-id="def38-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="def38-111">A continuación se deberán seguir las reglas para la implementación de Collate.</span><span class="sxs-lookup"><span data-stu-id="def38-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="def38-112">Definición y reglas de elementos</span><span class="sxs-lookup"><span data-stu-id="def38-112">Element Definition and Rules</span></span>

<span data-ttu-id="def38-113">Primero debe seguir las reglas de JobCollateAllDocument y, a continuación, aplicar las reglas de DocumentCollate para que los escenarios funcionen.</span><span class="sxs-lookup"><span data-stu-id="def38-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="def38-114">Tenga en cuenta que en un valor de conversión PrintTicket a Devmode, donde JobCollateAllDocuments no es compatible con el controlador, es el controlador el que elige el comportamiento adecuado que se debe tomar (JobCollateAllDocuments = ON u OFF).</span><span class="sxs-lookup"><span data-stu-id="def38-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="def38-115">Además, la opción se puede cambiar en función de otras opciones de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="def38-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="def38-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="def38-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="def38-117">ON: imprima (DocumentCopiesAllPages) copias de cada documento, repita JobCopiesAllDocuments veces.</span><span class="sxs-lookup"><span data-stu-id="def38-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="def38-118">OFF: para cada documento, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntos.</span><span class="sxs-lookup"><span data-stu-id="def38-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="def38-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="def38-119">DocumentCollate</span></span>

<span data-ttu-id="def38-120">ON: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de un documento impreso de forma contigua, intercala las hojas de ese documento.</span><span class="sxs-lookup"><span data-stu-id="def38-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="def38-121">OFF: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) impresas de forma contigua, imprima todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada hoja juntas.</span><span class="sxs-lookup"><span data-stu-id="def38-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="def38-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="def38-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="def38-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="def38-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="def38-124">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="def38-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="def38-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="def38-125">Element Information</span></span>



| <span data-ttu-id="def38-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="def38-126">Name</span></span> | <span data-ttu-id="def38-127">Valor</span><span class="sxs-lookup"><span data-stu-id="def38-127">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="def38-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="def38-128">Element Type</span></span> <br/>   | <span data-ttu-id="def38-129">Característica</span><span class="sxs-lookup"><span data-stu-id="def38-129">Feature</span></span><br/> |
| <span data-ttu-id="def38-130">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="def38-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="def38-131">Trabajo</span><span class="sxs-lookup"><span data-stu-id="def38-131">Job</span></span><br/>     |
| <span data-ttu-id="def38-132">Notas</span><span class="sxs-lookup"><span data-stu-id="def38-132">Notes</span></span> <br/>          | <span data-ttu-id="def38-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="def38-133">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="def38-134">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="def38-134">Structural Content</span></span>

<span data-ttu-id="def38-135">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="def38-135">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a><span data-ttu-id="def38-136">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="def38-136">Structure Variables</span></span>

<span data-ttu-id="def38-137">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="def38-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="def38-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="def38-138">Name</span></span>                               | <span data-ttu-id="def38-139">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="def38-139">Data type</span></span>         | <span data-ttu-id="def38-140">Unidad</span><span class="sxs-lookup"><span data-stu-id="def38-140">Unit</span></span>                  | <span data-ttu-id="def38-141">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="def38-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="def38-142">Resumen</span><span class="sxs-lookup"><span data-stu-id="def38-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="def38-143">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="def38-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="def38-144">string</span><span class="sxs-lookup"><span data-stu-id="def38-144">string</span></span><br/> | <span data-ttu-id="def38-145">caracteres</span><span class="sxs-lookup"><span data-stu-id="def38-145">characters</span></span><br/> | <span data-ttu-id="def38-146">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="def38-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="def38-147">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="def38-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="def38-148">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="def38-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="def38-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="def38-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="def38-150">string</span><span class="sxs-lookup"><span data-stu-id="def38-150">string</span></span><br/> | <span data-ttu-id="def38-151">N/D</span><span class="sxs-lookup"><span data-stu-id="def38-151">n/a</span></span><br/>        | <span data-ttu-id="def38-152">True, False.</span><span class="sxs-lookup"><span data-stu-id="def38-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="def38-153">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="def38-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="def38-154">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="def38-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="def38-155">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="def38-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="def38-156">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="def38-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




