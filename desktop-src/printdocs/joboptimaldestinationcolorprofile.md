---
description: Obtenga información sobre el elemento JobOptimalDestinationColorProfile que especifica el perfil de color óptimo dada la configuración actual del dispositivo.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408848"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="0c632-103">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="0c632-103">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="0c632-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="0c632-104">This topic is not current.</span></span> <span data-ttu-id="0c632-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0c632-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c632-106">Especifica el perfil de color óptimo dada la configuración actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c632-106">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="0c632-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0c632-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c632-108">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0c632-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0c632-109">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0c632-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0c632-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0c632-110">Element Information</span></span>



| <span data-ttu-id="0c632-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c632-111">Name</span></span> | <span data-ttu-id="0c632-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0c632-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="0c632-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0c632-113">Element Type</span></span> <br/>   | <span data-ttu-id="0c632-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c632-114">Property</span></span><br/> |
| <span data-ttu-id="0c632-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="0c632-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c632-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="0c632-116">Job</span></span><br/>      |
| <span data-ttu-id="0c632-117">Notas</span><span class="sxs-lookup"><span data-stu-id="0c632-117">Notes</span></span> <br/>          | <span data-ttu-id="0c632-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0c632-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="0c632-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0c632-119">Structural Content</span></span>

<span data-ttu-id="0c632-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="0c632-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0c632-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="0c632-121">Structure Variables</span></span>

<span data-ttu-id="0c632-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="0c632-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c632-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c632-123">Name</span></span>                            | <span data-ttu-id="0c632-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c632-124">Data type</span></span>         | <span data-ttu-id="0c632-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="0c632-125">Unit</span></span>           | <span data-ttu-id="0c632-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="0c632-126">Supported values</span></span>          | <span data-ttu-id="0c632-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="0c632-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="0c632-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="0c632-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="0c632-129">string</span><span class="sxs-lookup"><span data-stu-id="0c632-129">string</span></span><br/> | <span data-ttu-id="0c632-130">N/D</span><span class="sxs-lookup"><span data-stu-id="0c632-130">n/a</span></span><br/> | <span data-ttu-id="0c632-131">RGB, RGB, RGB, CCI</span><span class="sxs-lookup"><span data-stu-id="0c632-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="0c632-132">Especifica el perfil de color.</span><span class="sxs-lookup"><span data-stu-id="0c632-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="0c632-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="0c632-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="0c632-134">string</span><span class="sxs-lookup"><span data-stu-id="0c632-134">string</span></span><br/> | <span data-ttu-id="0c632-135">N/D</span><span class="sxs-lookup"><span data-stu-id="0c632-135">n/a</span></span><br/> | <span data-ttu-id="0c632-136">N/D</span><span class="sxs-lookup"><span data-stu-id="0c632-136">n/a</span></span><br/>            | <span data-ttu-id="0c632-137">Especifica la ruta de acceso del archivo al perfil.</span><span class="sxs-lookup"><span data-stu-id="0c632-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="0c632-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="0c632-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="0c632-139">string</span><span class="sxs-lookup"><span data-stu-id="0c632-139">string</span></span><br/> | <span data-ttu-id="0c632-140">N/D</span><span class="sxs-lookup"><span data-stu-id="0c632-140">n/a</span></span><br/> | <span data-ttu-id="0c632-141">N/D</span><span class="sxs-lookup"><span data-stu-id="0c632-141">n/a</span></span><br/>            | <span data-ttu-id="0c632-142">Contiene contenido de datos de perfil.</span><span class="sxs-lookup"><span data-stu-id="0c632-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0c632-143">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0c632-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0c632-144">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="0c632-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0c632-145">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="0c632-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0c632-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c632-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c632-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0c632-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




