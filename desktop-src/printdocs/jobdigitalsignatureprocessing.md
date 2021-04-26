---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998292"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="d3f22-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="d3f22-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="d3f22-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d3f22-105">This topic is not current.</span></span> <span data-ttu-id="d3f22-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d3f22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d3f22-107">Describe la configuración del procesamiento de firmas digitales para todo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d3f22-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="d3f22-108">Solo se aplica al contenido que contiene firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="d3f22-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="d3f22-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d3f22-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d3f22-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d3f22-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="d3f22-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d3f22-111">Element Information</span></span>



| <span data-ttu-id="d3f22-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3f22-112">Name</span></span> | <span data-ttu-id="d3f22-113">Value</span><span class="sxs-lookup"><span data-stu-id="d3f22-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d3f22-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d3f22-114">Element Type</span></span> <br/>   | <span data-ttu-id="d3f22-115">Característica</span><span class="sxs-lookup"><span data-stu-id="d3f22-115">Feature</span></span><br/> |
| <span data-ttu-id="d3f22-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d3f22-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d3f22-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="d3f22-117">Job</span></span><br/>     |
| <span data-ttu-id="d3f22-118">Notas</span><span class="sxs-lookup"><span data-stu-id="d3f22-118">Notes</span></span> <br/>          | <span data-ttu-id="d3f22-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d3f22-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d3f22-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d3f22-120">Structural Content</span></span>

<span data-ttu-id="d3f22-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d3f22-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="d3f22-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="d3f22-122">Structure Variables</span></span>

<span data-ttu-id="d3f22-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d3f22-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d3f22-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3f22-124">Name</span></span>                               | <span data-ttu-id="d3f22-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d3f22-125">Data type</span></span>         | <span data-ttu-id="d3f22-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="d3f22-126">Unit</span></span>                   | <span data-ttu-id="d3f22-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="d3f22-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d3f22-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="d3f22-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d3f22-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d3f22-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d3f22-130">string</span><span class="sxs-lookup"><span data-stu-id="d3f22-130">string</span></span><br/> | <span data-ttu-id="d3f22-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="d3f22-131">characters</span></span> <br/> | <span data-ttu-id="d3f22-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d3f22-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d3f22-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d3f22-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d3f22-134">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="d3f22-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="d3f22-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d3f22-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d3f22-136">string</span><span class="sxs-lookup"><span data-stu-id="d3f22-136">string</span></span><br/> | <span data-ttu-id="d3f22-137">N/D</span><span class="sxs-lookup"><span data-stu-id="d3f22-137">n/a</span></span><br/>         | <span data-ttu-id="d3f22-138">True, False</span><span class="sxs-lookup"><span data-stu-id="d3f22-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="d3f22-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="d3f22-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d3f22-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d3f22-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d3f22-141">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="d3f22-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d3f22-142">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="d3f22-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d3f22-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3f22-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f22-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d3f22-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




