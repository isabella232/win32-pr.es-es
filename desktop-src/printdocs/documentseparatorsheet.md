---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6bd0d58c5b361b167d22c672b7e080e4498d3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997062"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="e3206-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="e3206-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="e3206-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e3206-105">This topic is not current.</span></span> <span data-ttu-id="e3206-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3206-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3206-107">Describe el uso de la hoja separadora para un documento.</span><span class="sxs-lookup"><span data-stu-id="e3206-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="e3206-108">Las hojas separadoras deben aparecer en la salida como se indica en la opción especificada a continuación.</span><span class="sxs-lookup"><span data-stu-id="e3206-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="e3206-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e3206-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3206-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e3206-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e3206-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e3206-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e3206-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e3206-112">Element Information</span></span>



| <span data-ttu-id="e3206-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3206-113">Name</span></span> | <span data-ttu-id="e3206-114">Value</span><span class="sxs-lookup"><span data-stu-id="e3206-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="e3206-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e3206-115">Element Type</span></span> <br/>   | <span data-ttu-id="e3206-116">Característica</span><span class="sxs-lookup"><span data-stu-id="e3206-116">Feature</span></span><br/>  |
| <span data-ttu-id="e3206-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e3206-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3206-118">Documento</span><span class="sxs-lookup"><span data-stu-id="e3206-118">Document</span></span><br/> |
| <span data-ttu-id="e3206-119">Notas</span><span class="sxs-lookup"><span data-stu-id="e3206-119">Notes</span></span> <br/>          | <span data-ttu-id="e3206-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3206-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="e3206-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e3206-121">Structural Content</span></span>

<span data-ttu-id="e3206-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e3206-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="e3206-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="e3206-123">Structure Variables</span></span>

<span data-ttu-id="e3206-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e3206-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3206-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3206-125">Name</span></span>                               | <span data-ttu-id="e3206-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e3206-126">Data type</span></span>         | <span data-ttu-id="e3206-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="e3206-127">Unit</span></span>                  | <span data-ttu-id="e3206-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="e3206-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e3206-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="e3206-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e3206-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e3206-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e3206-131">string</span><span class="sxs-lookup"><span data-stu-id="e3206-131">string</span></span><br/> | <span data-ttu-id="e3206-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="e3206-132">characters</span></span><br/> | <span data-ttu-id="e3206-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e3206-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e3206-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e3206-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e3206-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="e3206-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e3206-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e3206-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e3206-137">string</span><span class="sxs-lookup"><span data-stu-id="e3206-137">string</span></span><br/> | <span data-ttu-id="e3206-138">N/D</span><span class="sxs-lookup"><span data-stu-id="e3206-138">n/a</span></span><br/>        | <span data-ttu-id="e3206-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="e3206-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e3206-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="e3206-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e3206-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e3206-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e3206-142">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="e3206-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e3206-143">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="e3206-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="e3206-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3206-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3206-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e3206-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




