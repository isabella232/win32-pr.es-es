---
description: Obtenga información sobre el elemento JobDigitalSignatureProcessing, que describe cómo configurar el procesamiento de firmas digitales para todo el trabajo.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9491a921d9d733dd0de0a4e5133d5c6690b2b4a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408948"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="5df6c-103">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="5df6c-103">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="5df6c-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5df6c-104">This topic is not current.</span></span> <span data-ttu-id="5df6c-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5df6c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5df6c-106">Describe la configuración del procesamiento de firmas digitales para todo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5df6c-106">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="5df6c-107">Solo se aplica al contenido que contiene firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="5df6c-107">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="5df6c-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5df6c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5df6c-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="5df6c-109">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="5df6c-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5df6c-110">Element Information</span></span>



| <span data-ttu-id="5df6c-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="5df6c-111">Name</span></span> | <span data-ttu-id="5df6c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5df6c-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5df6c-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5df6c-113">Element Type</span></span> <br/>   | <span data-ttu-id="5df6c-114">Característica</span><span class="sxs-lookup"><span data-stu-id="5df6c-114">Feature</span></span><br/> |
| <span data-ttu-id="5df6c-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5df6c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5df6c-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="5df6c-116">Job</span></span><br/>     |
| <span data-ttu-id="5df6c-117">Notas</span><span class="sxs-lookup"><span data-stu-id="5df6c-117">Notes</span></span> <br/>          | <span data-ttu-id="5df6c-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5df6c-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5df6c-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="5df6c-119">Structural Content</span></span>

<span data-ttu-id="5df6c-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5df6c-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5df6c-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="5df6c-121">Structure Variables</span></span>

<span data-ttu-id="5df6c-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5df6c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5df6c-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="5df6c-123">Name</span></span>                               | <span data-ttu-id="5df6c-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5df6c-124">Data type</span></span>         | <span data-ttu-id="5df6c-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="5df6c-125">Unit</span></span>                   | <span data-ttu-id="5df6c-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="5df6c-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5df6c-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="5df6c-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5df6c-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5df6c-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5df6c-129">string</span><span class="sxs-lookup"><span data-stu-id="5df6c-129">string</span></span><br/> | <span data-ttu-id="5df6c-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="5df6c-130">characters</span></span> <br/> | <span data-ttu-id="5df6c-131">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5df6c-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5df6c-132">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5df6c-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5df6c-133">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="5df6c-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="5df6c-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5df6c-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5df6c-135">string</span><span class="sxs-lookup"><span data-stu-id="5df6c-135">string</span></span><br/> | <span data-ttu-id="5df6c-136">N/D</span><span class="sxs-lookup"><span data-stu-id="5df6c-136">n/a</span></span><br/>         | <span data-ttu-id="5df6c-137">True, False</span><span class="sxs-lookup"><span data-stu-id="5df6c-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="5df6c-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="5df6c-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5df6c-139">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5df6c-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5df6c-140">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="5df6c-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5df6c-141">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="5df6c-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5df6c-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5df6c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5df6c-143">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5df6c-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




