---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825120996d0d488af347ed871386a12d7f8014a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997892"
---
# <a name="documentholepunch"></a><span data-ttu-id="9bda2-104">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="9bda2-104">DocumentHolePunch</span></span>

<span data-ttu-id="9bda2-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9bda2-105">This topic is not current.</span></span> <span data-ttu-id="9bda2-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9bda2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9bda2-107">Describe las características de los huecos de la salida.</span><span class="sxs-lookup"><span data-stu-id="9bda2-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="9bda2-108">Cada documento se explica por separado.</span><span class="sxs-lookup"><span data-stu-id="9bda2-108">Each document is punched separately.</span></span> <span data-ttu-id="9bda2-109">Las palabras clave JobHolePunch y DocumentHolePunch son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="9bda2-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="9bda2-110">Ambos no deben especificarse simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="9bda2-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9bda2-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9bda2-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9bda2-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9bda2-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9bda2-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9bda2-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9bda2-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9bda2-114">Element Information</span></span>



| <span data-ttu-id="9bda2-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bda2-115">Name</span></span> | <span data-ttu-id="9bda2-116">Value</span><span class="sxs-lookup"><span data-stu-id="9bda2-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="9bda2-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9bda2-117">Element Type</span></span> <br/>   | <span data-ttu-id="9bda2-118">Característica</span><span class="sxs-lookup"><span data-stu-id="9bda2-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="9bda2-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9bda2-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9bda2-120">Documento</span><span class="sxs-lookup"><span data-stu-id="9bda2-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="9bda2-121">Notas</span><span class="sxs-lookup"><span data-stu-id="9bda2-121">Notes</span></span> <br/>          | <span data-ttu-id="9bda2-122">Top, Bottom, Left y Right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="9bda2-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9bda2-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9bda2-123">Structural Content</span></span>

<span data-ttu-id="9bda2-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9bda2-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="9bda2-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9bda2-125">Structure Variables</span></span>

<span data-ttu-id="9bda2-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9bda2-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9bda2-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bda2-127">Name</span></span>                               | <span data-ttu-id="9bda2-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9bda2-128">Data type</span></span>         | <span data-ttu-id="9bda2-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="9bda2-129">Unit</span></span>                  | <span data-ttu-id="9bda2-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9bda2-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9bda2-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="9bda2-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9bda2-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9bda2-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9bda2-133">string</span><span class="sxs-lookup"><span data-stu-id="9bda2-133">string</span></span><br/> | <span data-ttu-id="9bda2-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="9bda2-134">characters</span></span><br/> | <span data-ttu-id="9bda2-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9bda2-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9bda2-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9bda2-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9bda2-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9bda2-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9bda2-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9bda2-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9bda2-139">string</span><span class="sxs-lookup"><span data-stu-id="9bda2-139">string</span></span><br/> | <span data-ttu-id="9bda2-140">N/D</span><span class="sxs-lookup"><span data-stu-id="9bda2-140">n/a</span></span><br/>        | <span data-ttu-id="9bda2-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="9bda2-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9bda2-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9bda2-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9bda2-143">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9bda2-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9bda2-144">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9bda2-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9bda2-145">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9bda2-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="9bda2-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bda2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bda2-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9bda2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




