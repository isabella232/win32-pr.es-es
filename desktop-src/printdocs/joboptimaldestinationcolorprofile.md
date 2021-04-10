---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954f67df5720e19de39d2c1c752c6d9eb860a502
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104003479"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="66579-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="66579-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="66579-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="66579-105">This topic is not current.</span></span> <span data-ttu-id="66579-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="66579-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="66579-107">Especifica el perfil de color óptimo según la configuración actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66579-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="66579-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="66579-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="66579-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="66579-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="66579-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="66579-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="66579-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="66579-111">Element Information</span></span>



| <span data-ttu-id="66579-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="66579-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="66579-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="66579-113">Element Type</span></span> <br/>   | <span data-ttu-id="66579-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66579-114">Property</span></span><br/> |
| <span data-ttu-id="66579-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="66579-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="66579-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="66579-116">Job</span></span><br/>      |
| <span data-ttu-id="66579-117">Notas</span><span class="sxs-lookup"><span data-stu-id="66579-117">Notes</span></span> <br/>          | <span data-ttu-id="66579-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="66579-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="66579-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="66579-119">Structural Content</span></span>

<span data-ttu-id="66579-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="66579-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="66579-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="66579-121">Structure Variables</span></span>

<span data-ttu-id="66579-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="66579-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="66579-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="66579-123">Name</span></span>                            | <span data-ttu-id="66579-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="66579-124">Data type</span></span>         | <span data-ttu-id="66579-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="66579-125">Unit</span></span>           | <span data-ttu-id="66579-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="66579-126">Supported values</span></span>          | <span data-ttu-id="66579-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="66579-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="66579-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="66579-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="66579-129">string</span><span class="sxs-lookup"><span data-stu-id="66579-129">string</span></span><br/> | <span data-ttu-id="66579-130">N/D</span><span class="sxs-lookup"><span data-stu-id="66579-130">n/a</span></span><br/> | <span data-ttu-id="66579-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="66579-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="66579-132">Especifica el perfil de color.</span><span class="sxs-lookup"><span data-stu-id="66579-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="66579-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="66579-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="66579-134">string</span><span class="sxs-lookup"><span data-stu-id="66579-134">string</span></span><br/> | <span data-ttu-id="66579-135">N/D</span><span class="sxs-lookup"><span data-stu-id="66579-135">n/a</span></span><br/> | <span data-ttu-id="66579-136">N/D</span><span class="sxs-lookup"><span data-stu-id="66579-136">n/a</span></span><br/>            | <span data-ttu-id="66579-137">Especifica la ruta de acceso del archivo al perfil.</span><span class="sxs-lookup"><span data-stu-id="66579-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="66579-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="66579-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="66579-139">string</span><span class="sxs-lookup"><span data-stu-id="66579-139">string</span></span><br/> | <span data-ttu-id="66579-140">N/D</span><span class="sxs-lookup"><span data-stu-id="66579-140">n/a</span></span><br/> | <span data-ttu-id="66579-141">N/D</span><span class="sxs-lookup"><span data-stu-id="66579-141">n/a</span></span><br/>            | <span data-ttu-id="66579-142">Contiene contenido de datos de perfil.</span><span class="sxs-lookup"><span data-stu-id="66579-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="66579-143">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="66579-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="66579-144">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="66579-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="66579-145">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="66579-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="66579-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66579-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66579-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="66579-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




