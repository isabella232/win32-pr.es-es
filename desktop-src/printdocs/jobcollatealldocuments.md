---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0406a5f9106cbe4cd2a8ccb0986a1bfacc95b916
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361981"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="49b8b-104">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="49b8b-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="49b8b-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="49b8b-105">This topic is not current.</span></span> <span data-ttu-id="49b8b-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49b8b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49b8b-107">Describe las características de intercalación de la salida.</span><span class="sxs-lookup"><span data-stu-id="49b8b-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="49b8b-108">Se intercalan todos los documentos de cada trabajo individual.</span><span class="sxs-lookup"><span data-stu-id="49b8b-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="49b8b-109">DocumentCollate y JobCollateAlldocuments se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="49b8b-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="49b8b-110">El comportamiento y la implementación de si se ha implementado o solo una de estas palabras clave se deja al controlador.</span><span class="sxs-lookup"><span data-stu-id="49b8b-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="49b8b-111">A continuación se muestran las reglas que deben seguirse para la implementación de intercalación.</span><span class="sxs-lookup"><span data-stu-id="49b8b-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="49b8b-112">Definición de elementos y reglas</span><span class="sxs-lookup"><span data-stu-id="49b8b-112">Element Definition and Rules</span></span>

<span data-ttu-id="49b8b-113">En primer lugar, debe seguir las reglas de JobCollateAllDocument y, a continuación, aplicar las reglas de DocumentCollate para que los escenarios funcionen.</span><span class="sxs-lookup"><span data-stu-id="49b8b-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="49b8b-114">Tenga en cuenta que en la configuración de la conversión de PrintTicket a DEVMODE, donde JobCollateAllDocuments no es compatible con el controlador, depende del controlador elegir el comportamiento adecuado que se debe llevar a cabo (JobCollateAllDocuments = ON u OFF).</span><span class="sxs-lookup"><span data-stu-id="49b8b-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="49b8b-115">Además, la opción se puede cambiar en función de otras opciones de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="49b8b-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="49b8b-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="49b8b-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="49b8b-117">EN: copias de impresión (DocumentCopiesAllPages) de cada documento, repita JobCopiesAllDocuments veces.</span><span class="sxs-lookup"><span data-stu-id="49b8b-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="49b8b-118">Desactivado: para cada documento, imprime (JobCopiesAllDocuments x DocumentCopiesAllPages) copias juntas.</span><span class="sxs-lookup"><span data-stu-id="49b8b-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="49b8b-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="49b8b-119">DocumentCollate</span></span>

<span data-ttu-id="49b8b-120">ACTIVADO: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de un documento que se imprime de forma contigua, intercalar hojas en dicho documento.</span><span class="sxs-lookup"><span data-stu-id="49b8b-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="49b8b-121">OFF: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) impresas de forma contigua, imprime todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada hoja juntas.</span><span class="sxs-lookup"><span data-stu-id="49b8b-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="49b8b-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="49b8b-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="49b8b-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="49b8b-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="49b8b-124">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="49b8b-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="49b8b-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="49b8b-125">Element Information</span></span>



| <span data-ttu-id="49b8b-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="49b8b-126">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="49b8b-127">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="49b8b-127">Element Type</span></span> <br/>   | <span data-ttu-id="49b8b-128">Característica</span><span class="sxs-lookup"><span data-stu-id="49b8b-128">Feature</span></span><br/> |
| <span data-ttu-id="49b8b-129">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="49b8b-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="49b8b-130">Trabajo</span><span class="sxs-lookup"><span data-stu-id="49b8b-130">Job</span></span><br/>     |
| <span data-ttu-id="49b8b-131">Notas</span><span class="sxs-lookup"><span data-stu-id="49b8b-131">Notes</span></span> <br/>          | <span data-ttu-id="49b8b-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="49b8b-132">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="49b8b-133">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="49b8b-133">Structural Content</span></span>

<span data-ttu-id="49b8b-134">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="49b8b-134">The XML structure of this element is:</span></span>

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

### <a name="structure-variables"></a><span data-ttu-id="49b8b-135">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="49b8b-135">Structure Variables</span></span>

<span data-ttu-id="49b8b-136">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="49b8b-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="49b8b-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="49b8b-137">Name</span></span>                               | <span data-ttu-id="49b8b-138">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="49b8b-138">Data type</span></span>         | <span data-ttu-id="49b8b-139">Unidad</span><span class="sxs-lookup"><span data-stu-id="49b8b-139">Unit</span></span>                  | <span data-ttu-id="49b8b-140">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="49b8b-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="49b8b-141">Resumen</span><span class="sxs-lookup"><span data-stu-id="49b8b-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="49b8b-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="49b8b-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="49b8b-143">string</span><span class="sxs-lookup"><span data-stu-id="49b8b-143">string</span></span><br/> | <span data-ttu-id="49b8b-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="49b8b-144">characters</span></span><br/> | <span data-ttu-id="49b8b-145">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="49b8b-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="49b8b-146">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="49b8b-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="49b8b-147">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="49b8b-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="49b8b-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="49b8b-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="49b8b-149">string</span><span class="sxs-lookup"><span data-stu-id="49b8b-149">string</span></span><br/> | <span data-ttu-id="49b8b-150">N/D</span><span class="sxs-lookup"><span data-stu-id="49b8b-150">n/a</span></span><br/>        | <span data-ttu-id="49b8b-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="49b8b-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="49b8b-152">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="49b8b-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="49b8b-153">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="49b8b-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="49b8b-154">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="49b8b-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="49b8b-155">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="49b8b-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

 

 




