---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eda63fe0d801bc1039af2c514c284440b1be47
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717447"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="74b29-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="74b29-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="74b29-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="74b29-105">This topic is not current.</span></span> <span data-ttu-id="74b29-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74b29-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74b29-107">Describe el método de corte para rollo de papel.</span><span class="sxs-lookup"><span data-stu-id="74b29-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="74b29-108">El rollo debe cortar al final del trabajo.</span><span class="sxs-lookup"><span data-stu-id="74b29-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="74b29-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="74b29-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="74b29-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="74b29-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="74b29-111">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="74b29-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="74b29-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="74b29-112">Element Information</span></span>



| <span data-ttu-id="74b29-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="74b29-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="74b29-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="74b29-114">Element Type</span></span> <br/>   | <span data-ttu-id="74b29-115">Característica</span><span class="sxs-lookup"><span data-stu-id="74b29-115">Feature</span></span><br/> |
| <span data-ttu-id="74b29-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="74b29-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="74b29-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="74b29-117">Job</span></span><br/>     |
| <span data-ttu-id="74b29-118">Notas</span><span class="sxs-lookup"><span data-stu-id="74b29-118">Notes</span></span> <br/>          | <span data-ttu-id="74b29-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="74b29-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="74b29-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="74b29-120">Structural Content</span></span>

<span data-ttu-id="74b29-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="74b29-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
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

## <a name="structure-variables"></a><span data-ttu-id="74b29-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="74b29-122">Structure Variables</span></span>

<span data-ttu-id="74b29-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="74b29-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="74b29-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="74b29-124">Name</span></span>                               | <span data-ttu-id="74b29-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="74b29-125">Data type</span></span>         | <span data-ttu-id="74b29-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="74b29-126">Unit</span></span>                  | <span data-ttu-id="74b29-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="74b29-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="74b29-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="74b29-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="74b29-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="74b29-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="74b29-130">string</span><span class="sxs-lookup"><span data-stu-id="74b29-130">string</span></span><br/> | <span data-ttu-id="74b29-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="74b29-131">characters</span></span><br/> | <span data-ttu-id="74b29-132">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="74b29-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="74b29-133">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="74b29-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="74b29-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="74b29-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="74b29-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="74b29-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="74b29-136">string</span><span class="sxs-lookup"><span data-stu-id="74b29-136">string</span></span><br/> | <span data-ttu-id="74b29-137">N/D</span><span class="sxs-lookup"><span data-stu-id="74b29-137">n/a</span></span><br/>        | <span data-ttu-id="74b29-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="74b29-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="74b29-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="74b29-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="74b29-140">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="74b29-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="74b29-141">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="74b29-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="74b29-142">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="74b29-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="74b29-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74b29-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b29-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="74b29-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




