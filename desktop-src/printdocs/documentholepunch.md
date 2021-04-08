---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42783248213f1ccffd0c0fb7f3a416ee6ae801d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104003483"
---
# <a name="documentholepunch"></a><span data-ttu-id="1c2b0-104">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="1c2b0-104">DocumentHolePunch</span></span>

<span data-ttu-id="1c2b0-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-105">This topic is not current.</span></span> <span data-ttu-id="1c2b0-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1c2b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1c2b0-107">Describe las características de perforación de agujeros de la salida.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="1c2b0-108">Cada documento se perfora por separado.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-108">Each document is punched separately.</span></span> <span data-ttu-id="1c2b0-109">Las palabras clave JobHolePunch y DocumentHolePunch se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="1c2b0-110">Ambos no se deben especificar simultáneamente en un documento de capacidades de impresión o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1c2b0-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1c2b0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1c2b0-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1c2b0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1c2b0-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="1c2b0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1c2b0-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1c2b0-114">Element Information</span></span>



| <span data-ttu-id="1c2b0-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c2b0-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1c2b0-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1c2b0-116">Element Type</span></span> <br/>   | <span data-ttu-id="1c2b0-117">Característica</span><span class="sxs-lookup"><span data-stu-id="1c2b0-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="1c2b0-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1c2b0-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1c2b0-119">Documento</span><span class="sxs-lookup"><span data-stu-id="1c2b0-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="1c2b0-120">Notas</span><span class="sxs-lookup"><span data-stu-id="1c2b0-120">Notes</span></span> <br/>          | <span data-ttu-id="1c2b0-121">Top, Bottom, left y right son relativos a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1c2b0-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1c2b0-122">Structural Content</span></span>

<span data-ttu-id="1c2b0-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="1c2b0-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1c2b0-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="1c2b0-124">Structure Variables</span></span>

<span data-ttu-id="1c2b0-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1c2b0-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c2b0-126">Name</span></span>                               | <span data-ttu-id="1c2b0-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1c2b0-127">Data type</span></span>         | <span data-ttu-id="1c2b0-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="1c2b0-128">Unit</span></span>                  | <span data-ttu-id="1c2b0-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="1c2b0-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1c2b0-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="1c2b0-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1c2b0-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1c2b0-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1c2b0-132">string</span><span class="sxs-lookup"><span data-stu-id="1c2b0-132">string</span></span><br/> | <span data-ttu-id="1c2b0-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="1c2b0-133">characters</span></span><br/> | <span data-ttu-id="1c2b0-134">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1c2b0-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1c2b0-135">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1c2b0-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1c2b0-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1c2b0-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1c2b0-138">string</span><span class="sxs-lookup"><span data-stu-id="1c2b0-138">string</span></span><br/> | <span data-ttu-id="1c2b0-139">N/D</span><span class="sxs-lookup"><span data-stu-id="1c2b0-139">n/a</span></span><br/>        | <span data-ttu-id="1c2b0-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1c2b0-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1c2b0-142">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="1c2b0-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1c2b0-143">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="1c2b0-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1c2b0-144">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="1c2b0-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1c2b0-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c2b0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c2b0-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1c2b0-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




