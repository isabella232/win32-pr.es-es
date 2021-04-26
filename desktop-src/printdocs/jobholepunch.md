---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56316c94dc56a2646446a8cd63885cceaa1407fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999302"
---
# <a name="jobholepunch"></a><span data-ttu-id="9a5e1-104">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="9a5e1-104">JobHolePunch</span></span>

<span data-ttu-id="9a5e1-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-105">This topic is not current.</span></span> <span data-ttu-id="9a5e1-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9a5e1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9a5e1-107">Describe las características de los huecos de la salida.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="9a5e1-108">Todos los documentos están juntos.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-108">All documents are punched together.</span></span> <span data-ttu-id="9a5e1-109">Las palabras clave JobHolePunch y DocumentHolePunch son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="9a5e1-110">Ambos no se deben especificar simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9a5e1-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9a5e1-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9a5e1-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9a5e1-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9a5e1-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9a5e1-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9a5e1-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9a5e1-114">Element Information</span></span>



| <span data-ttu-id="9a5e1-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a5e1-115">Name</span></span> | <span data-ttu-id="9a5e1-116">Value</span><span class="sxs-lookup"><span data-stu-id="9a5e1-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5e1-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9a5e1-117">Element Type</span></span> <br/>   | <span data-ttu-id="9a5e1-118">Característica</span><span class="sxs-lookup"><span data-stu-id="9a5e1-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="9a5e1-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9a5e1-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9a5e1-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="9a5e1-120">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="9a5e1-121">Notas</span><span class="sxs-lookup"><span data-stu-id="9a5e1-121">Notes</span></span> <br/>          | <span data-ttu-id="9a5e1-122">Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica mediante el origen del eje X y el eje Y.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9a5e1-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9a5e1-123">Structural Content</span></span>

<span data-ttu-id="9a5e1-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9a5e1-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="9a5e1-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9a5e1-125">Structure Variables</span></span>

<span data-ttu-id="9a5e1-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9a5e1-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a5e1-127">Name</span></span>                               | <span data-ttu-id="9a5e1-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9a5e1-128">Data type</span></span>         | <span data-ttu-id="9a5e1-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="9a5e1-129">Unit</span></span>                  | <span data-ttu-id="9a5e1-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9a5e1-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9a5e1-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="9a5e1-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9a5e1-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9a5e1-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9a5e1-133">string</span><span class="sxs-lookup"><span data-stu-id="9a5e1-133">string</span></span><br/> | <span data-ttu-id="9a5e1-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="9a5e1-134">characters</span></span><br/> | <span data-ttu-id="9a5e1-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="9a5e1-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9a5e1-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9a5e1-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9a5e1-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9a5e1-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9a5e1-139">string</span><span class="sxs-lookup"><span data-stu-id="9a5e1-139">string</span></span><br/> | <span data-ttu-id="9a5e1-140">N/D</span><span class="sxs-lookup"><span data-stu-id="9a5e1-140">n/a</span></span><br/>        | <span data-ttu-id="9a5e1-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9a5e1-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9a5e1-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9a5e1-143">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9a5e1-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9a5e1-144">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9a5e1-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9a5e1-145">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9a5e1-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="9a5e1-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a5e1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5e1-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9a5e1-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




