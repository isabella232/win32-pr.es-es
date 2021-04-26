---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999258"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="31dce-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="31dce-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="31dce-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="31dce-105">This topic is not current.</span></span> <span data-ttu-id="31dce-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="31dce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="31dce-107">Especifica el perfil de color óptimo dada la configuración actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31dce-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="31dce-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="31dce-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="31dce-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="31dce-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="31dce-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="31dce-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="31dce-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="31dce-111">Element Information</span></span>



| <span data-ttu-id="31dce-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="31dce-112">Name</span></span> | <span data-ttu-id="31dce-113">Value</span><span class="sxs-lookup"><span data-stu-id="31dce-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="31dce-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="31dce-114">Element Type</span></span> <br/>   | <span data-ttu-id="31dce-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31dce-115">Property</span></span><br/> |
| <span data-ttu-id="31dce-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="31dce-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="31dce-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="31dce-117">Job</span></span><br/>      |
| <span data-ttu-id="31dce-118">Notas</span><span class="sxs-lookup"><span data-stu-id="31dce-118">Notes</span></span> <br/>          | <span data-ttu-id="31dce-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="31dce-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="31dce-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="31dce-120">Structural Content</span></span>

<span data-ttu-id="31dce-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="31dce-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="31dce-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="31dce-122">Structure Variables</span></span>

<span data-ttu-id="31dce-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="31dce-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="31dce-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="31dce-124">Name</span></span>                            | <span data-ttu-id="31dce-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="31dce-125">Data type</span></span>         | <span data-ttu-id="31dce-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="31dce-126">Unit</span></span>           | <span data-ttu-id="31dce-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="31dce-127">Supported values</span></span>          | <span data-ttu-id="31dce-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="31dce-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="31dce-129">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="31dce-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="31dce-130">string</span><span class="sxs-lookup"><span data-stu-id="31dce-130">string</span></span><br/> | <span data-ttu-id="31dce-131">N/D</span><span class="sxs-lookup"><span data-stu-id="31dce-131">n/a</span></span><br/> | <span data-ttu-id="31dce-132">RGB, RGB, RGB, RGB</span><span class="sxs-lookup"><span data-stu-id="31dce-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="31dce-133">Especifica el perfil de color.</span><span class="sxs-lookup"><span data-stu-id="31dce-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="31dce-134">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="31dce-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="31dce-135">string</span><span class="sxs-lookup"><span data-stu-id="31dce-135">string</span></span><br/> | <span data-ttu-id="31dce-136">N/D</span><span class="sxs-lookup"><span data-stu-id="31dce-136">n/a</span></span><br/> | <span data-ttu-id="31dce-137">N/D</span><span class="sxs-lookup"><span data-stu-id="31dce-137">n/a</span></span><br/>            | <span data-ttu-id="31dce-138">Especifica la ruta de acceso del archivo al perfil.</span><span class="sxs-lookup"><span data-stu-id="31dce-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="31dce-139">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="31dce-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="31dce-140">string</span><span class="sxs-lookup"><span data-stu-id="31dce-140">string</span></span><br/> | <span data-ttu-id="31dce-141">N/D</span><span class="sxs-lookup"><span data-stu-id="31dce-141">n/a</span></span><br/> | <span data-ttu-id="31dce-142">N/D</span><span class="sxs-lookup"><span data-stu-id="31dce-142">n/a</span></span><br/>            | <span data-ttu-id="31dce-143">Contiene contenido de datos de perfil.</span><span class="sxs-lookup"><span data-stu-id="31dce-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="31dce-144">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="31dce-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="31dce-145">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="31dce-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="31dce-146">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="31dce-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="31dce-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31dce-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31dce-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="31dce-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




