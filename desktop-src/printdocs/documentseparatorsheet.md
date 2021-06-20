---
description: Obtenga información sobre el elemento DocumentSeparatorSheet, que describe el uso de la hoja separadora de un documento.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38195c2d1c52e5c02d9da4844b5fa981866a61bc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409168"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="046e1-103">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="046e1-103">DocumentSeparatorSheet</span></span>

<span data-ttu-id="046e1-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="046e1-104">This topic is not current.</span></span> <span data-ttu-id="046e1-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="046e1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="046e1-106">Describe el uso de la hoja separadora para un documento.</span><span class="sxs-lookup"><span data-stu-id="046e1-106">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="046e1-107">Las hojas separadoras deben aparecer en la salida como se indica en la opción especificada a continuación.</span><span class="sxs-lookup"><span data-stu-id="046e1-107">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="046e1-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="046e1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="046e1-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="046e1-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="046e1-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="046e1-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="046e1-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="046e1-111">Element Information</span></span>



| <span data-ttu-id="046e1-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="046e1-112">Name</span></span> | <span data-ttu-id="046e1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="046e1-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="046e1-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="046e1-114">Element Type</span></span> <br/>   | <span data-ttu-id="046e1-115">Característica</span><span class="sxs-lookup"><span data-stu-id="046e1-115">Feature</span></span><br/>  |
| <span data-ttu-id="046e1-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="046e1-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="046e1-117">Documento</span><span class="sxs-lookup"><span data-stu-id="046e1-117">Document</span></span><br/> |
| <span data-ttu-id="046e1-118">Notas</span><span class="sxs-lookup"><span data-stu-id="046e1-118">Notes</span></span> <br/>          | <span data-ttu-id="046e1-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="046e1-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="046e1-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="046e1-120">Structural Content</span></span>

<span data-ttu-id="046e1-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="046e1-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="046e1-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="046e1-122">Structure Variables</span></span>

<span data-ttu-id="046e1-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="046e1-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="046e1-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="046e1-124">Name</span></span>                               | <span data-ttu-id="046e1-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="046e1-125">Data type</span></span>         | <span data-ttu-id="046e1-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="046e1-126">Unit</span></span>                  | <span data-ttu-id="046e1-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="046e1-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="046e1-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="046e1-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="046e1-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="046e1-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="046e1-130">string</span><span class="sxs-lookup"><span data-stu-id="046e1-130">string</span></span><br/> | <span data-ttu-id="046e1-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="046e1-131">characters</span></span><br/> | <span data-ttu-id="046e1-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="046e1-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="046e1-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="046e1-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="046e1-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="046e1-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="046e1-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="046e1-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="046e1-136">string</span><span class="sxs-lookup"><span data-stu-id="046e1-136">string</span></span><br/> | <span data-ttu-id="046e1-137">N/D</span><span class="sxs-lookup"><span data-stu-id="046e1-137">n/a</span></span><br/>        | <span data-ttu-id="046e1-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="046e1-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="046e1-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="046e1-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="046e1-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="046e1-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="046e1-141">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="046e1-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="046e1-142">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="046e1-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="046e1-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="046e1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="046e1-144">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="046e1-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




