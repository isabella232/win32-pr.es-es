---
description: Obtenga información sobre el elemento DocumentRollCut, que describe el método de corte para el papel. Cada documento se controla por separado.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f7232cbe9dafce25aa2ee482ca40bf99145841
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409188"
---
# <a name="documentrollcut"></a><span data-ttu-id="efd09-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="efd09-104">DocumentRollCut</span></span>

<span data-ttu-id="efd09-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="efd09-105">This topic is not current.</span></span> <span data-ttu-id="efd09-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="efd09-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="efd09-107">Describe el método de corte para el papel de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="efd09-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="efd09-108">Cada documento se controla por separado.</span><span class="sxs-lookup"><span data-stu-id="efd09-108">Each document is handled separately.</span></span> <span data-ttu-id="efd09-109">Las opciones especificadas describen los distintos métodos para el corte de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="efd09-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="efd09-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="efd09-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="efd09-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="efd09-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="efd09-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="efd09-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="efd09-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="efd09-113">Element Information</span></span>



| <span data-ttu-id="efd09-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="efd09-114">Name</span></span> | <span data-ttu-id="efd09-115">Valor</span><span class="sxs-lookup"><span data-stu-id="efd09-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="efd09-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="efd09-116">Element Type</span></span> <br/>   | <span data-ttu-id="efd09-117">Característica</span><span class="sxs-lookup"><span data-stu-id="efd09-117">Feature</span></span><br/>  |
| <span data-ttu-id="efd09-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="efd09-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="efd09-119">Documento</span><span class="sxs-lookup"><span data-stu-id="efd09-119">Document</span></span><br/> |
| <span data-ttu-id="efd09-120">Notas</span><span class="sxs-lookup"><span data-stu-id="efd09-120">Notes</span></span> <br/>          | <span data-ttu-id="efd09-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="efd09-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="efd09-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="efd09-122">Structural Content</span></span>

<span data-ttu-id="efd09-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="efd09-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="efd09-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="efd09-124">Structure Variables</span></span>

<span data-ttu-id="efd09-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="efd09-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="efd09-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="efd09-126">Name</span></span>                               | <span data-ttu-id="efd09-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="efd09-127">Data type</span></span>         | <span data-ttu-id="efd09-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="efd09-128">Unit</span></span>                  | <span data-ttu-id="efd09-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="efd09-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="efd09-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="efd09-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="efd09-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="efd09-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="efd09-132">string</span><span class="sxs-lookup"><span data-stu-id="efd09-132">string</span></span><br/> | <span data-ttu-id="efd09-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="efd09-133">characters</span></span><br/> | <span data-ttu-id="efd09-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="efd09-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="efd09-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="efd09-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="efd09-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="efd09-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="efd09-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="efd09-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="efd09-138">string</span><span class="sxs-lookup"><span data-stu-id="efd09-138">string</span></span><br/> | <span data-ttu-id="efd09-139">N/D</span><span class="sxs-lookup"><span data-stu-id="efd09-139">n/a</span></span><br/>        | <span data-ttu-id="efd09-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="efd09-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="efd09-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="efd09-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="efd09-142">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="efd09-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="efd09-143">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="efd09-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="efd09-144">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="efd09-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="efd09-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efd09-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efd09-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="efd09-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




