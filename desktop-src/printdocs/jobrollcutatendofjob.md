---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178b045546552048b2a66a1c0824645c1720b1a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993942"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="1f56f-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="1f56f-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="1f56f-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1f56f-105">This topic is not current.</span></span> <span data-ttu-id="1f56f-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1f56f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f56f-107">Describe el método de corte para el papel.</span><span class="sxs-lookup"><span data-stu-id="1f56f-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="1f56f-108">El lanzamiento se debe cortar al final del trabajo.</span><span class="sxs-lookup"><span data-stu-id="1f56f-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="1f56f-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1f56f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1f56f-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1f56f-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1f56f-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1f56f-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1f56f-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1f56f-112">Element Information</span></span>



| <span data-ttu-id="1f56f-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f56f-113">Name</span></span> | <span data-ttu-id="1f56f-114">Value</span><span class="sxs-lookup"><span data-stu-id="1f56f-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1f56f-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1f56f-115">Element Type</span></span> <br/>   | <span data-ttu-id="1f56f-116">Característica</span><span class="sxs-lookup"><span data-stu-id="1f56f-116">Feature</span></span><br/> |
| <span data-ttu-id="1f56f-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1f56f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1f56f-118">Trabajo</span><span class="sxs-lookup"><span data-stu-id="1f56f-118">Job</span></span><br/>     |
| <span data-ttu-id="1f56f-119">Notas</span><span class="sxs-lookup"><span data-stu-id="1f56f-119">Notes</span></span> <br/>          | <span data-ttu-id="1f56f-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1f56f-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1f56f-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1f56f-121">Structural Content</span></span>

<span data-ttu-id="1f56f-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="1f56f-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1f56f-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="1f56f-123">Structure Variables</span></span>

<span data-ttu-id="1f56f-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1f56f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1f56f-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f56f-125">Name</span></span>                               | <span data-ttu-id="1f56f-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1f56f-126">Data type</span></span>         | <span data-ttu-id="1f56f-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="1f56f-127">Unit</span></span>                  | <span data-ttu-id="1f56f-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="1f56f-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1f56f-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="1f56f-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1f56f-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1f56f-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1f56f-131">string</span><span class="sxs-lookup"><span data-stu-id="1f56f-131">string</span></span><br/> | <span data-ttu-id="1f56f-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="1f56f-132">characters</span></span><br/> | <span data-ttu-id="1f56f-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="1f56f-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1f56f-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1f56f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1f56f-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1f56f-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1f56f-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1f56f-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1f56f-137">string</span><span class="sxs-lookup"><span data-stu-id="1f56f-137">string</span></span><br/> | <span data-ttu-id="1f56f-138">N/D</span><span class="sxs-lookup"><span data-stu-id="1f56f-138">n/a</span></span><br/>        | <span data-ttu-id="1f56f-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="1f56f-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1f56f-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1f56f-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1f56f-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1f56f-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1f56f-142">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="1f56f-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1f56f-143">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="1f56f-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1f56f-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f56f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f56f-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1f56f-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




