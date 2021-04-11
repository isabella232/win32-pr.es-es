---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a20c02c50638d532660845efc1b3894f4a7e1
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279906"
---
# <a name="documentrollcut"></a><span data-ttu-id="afaed-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="afaed-104">DocumentRollCut</span></span>

<span data-ttu-id="afaed-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="afaed-105">This topic is not current.</span></span> <span data-ttu-id="afaed-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="afaed-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="afaed-107">Describe el método de corte para rollo de papel.</span><span class="sxs-lookup"><span data-stu-id="afaed-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="afaed-108">Cada documento se administra por separado.</span><span class="sxs-lookup"><span data-stu-id="afaed-108">Each document is handled separately.</span></span> <span data-ttu-id="afaed-109">Las opciones especificadas describen los distintos métodos para el corte del rollo.</span><span class="sxs-lookup"><span data-stu-id="afaed-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="afaed-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="afaed-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="afaed-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="afaed-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="afaed-112">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="afaed-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="afaed-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="afaed-113">Element Information</span></span>



| <span data-ttu-id="afaed-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="afaed-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="afaed-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="afaed-115">Element Type</span></span> <br/>   | <span data-ttu-id="afaed-116">Característica</span><span class="sxs-lookup"><span data-stu-id="afaed-116">Feature</span></span><br/>  |
| <span data-ttu-id="afaed-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="afaed-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="afaed-118">Documento</span><span class="sxs-lookup"><span data-stu-id="afaed-118">Document</span></span><br/> |
| <span data-ttu-id="afaed-119">Notas</span><span class="sxs-lookup"><span data-stu-id="afaed-119">Notes</span></span> <br/>          | <span data-ttu-id="afaed-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="afaed-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="afaed-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="afaed-121">Structural Content</span></span>

<span data-ttu-id="afaed-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="afaed-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
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

## <a name="structure-variables"></a><span data-ttu-id="afaed-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="afaed-123">Structure Variables</span></span>

<span data-ttu-id="afaed-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="afaed-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="afaed-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="afaed-125">Name</span></span>                               | <span data-ttu-id="afaed-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="afaed-126">Data type</span></span>         | <span data-ttu-id="afaed-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="afaed-127">Unit</span></span>                  | <span data-ttu-id="afaed-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="afaed-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="afaed-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="afaed-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="afaed-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="afaed-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="afaed-131">string</span><span class="sxs-lookup"><span data-stu-id="afaed-131">string</span></span><br/> | <span data-ttu-id="afaed-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="afaed-132">characters</span></span><br/> | <span data-ttu-id="afaed-133">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="afaed-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="afaed-134">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="afaed-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="afaed-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="afaed-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="afaed-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="afaed-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="afaed-137">string</span><span class="sxs-lookup"><span data-stu-id="afaed-137">string</span></span><br/> | <span data-ttu-id="afaed-138">N/D</span><span class="sxs-lookup"><span data-stu-id="afaed-138">n/a</span></span><br/>        | <span data-ttu-id="afaed-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="afaed-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="afaed-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="afaed-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="afaed-141">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="afaed-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="afaed-142">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="afaed-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="afaed-143">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="afaed-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="afaed-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="afaed-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afaed-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="afaed-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




