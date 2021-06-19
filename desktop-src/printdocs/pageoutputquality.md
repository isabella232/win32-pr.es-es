---
description: Obtenga información sobre el elemento configurable por el usuario PageOutputQuality. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395599"
---
# <a name="pageoutputquality"></a><span data-ttu-id="ce08d-105">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="ce08d-105">PageOutputQuality</span></span>

<span data-ttu-id="ce08d-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ce08d-106">This topic is not current.</span></span> <span data-ttu-id="ce08d-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ce08d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce08d-108">Describe el nivel de calidad de la salida.</span><span class="sxs-lookup"><span data-stu-id="ce08d-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="ce08d-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ce08d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ce08d-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ce08d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ce08d-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ce08d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ce08d-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ce08d-112">Element Information</span></span>



| <span data-ttu-id="ce08d-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce08d-113">Name</span></span> | <span data-ttu-id="ce08d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ce08d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ce08d-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ce08d-115">Element Type</span></span> <br/>   | <span data-ttu-id="ce08d-116">Característica</span><span class="sxs-lookup"><span data-stu-id="ce08d-116">Feature</span></span><br/> |
| <span data-ttu-id="ce08d-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ce08d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce08d-118">Página</span><span class="sxs-lookup"><span data-stu-id="ce08d-118">Page</span></span><br/>    |
| <span data-ttu-id="ce08d-119">Notas</span><span class="sxs-lookup"><span data-stu-id="ce08d-119">Notes</span></span> <br/>          | <span data-ttu-id="ce08d-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ce08d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ce08d-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ce08d-121">Structural Content</span></span>

<span data-ttu-id="ce08d-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ce08d-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="ce08d-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="ce08d-123">Structure Variables</span></span>

<span data-ttu-id="ce08d-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ce08d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce08d-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce08d-125">Name</span></span>                               | <span data-ttu-id="ce08d-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ce08d-126">Data type</span></span>         | <span data-ttu-id="ce08d-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="ce08d-127">Unit</span></span>                  | <span data-ttu-id="ce08d-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="ce08d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ce08d-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="ce08d-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ce08d-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ce08d-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ce08d-131">string</span><span class="sxs-lookup"><span data-stu-id="ce08d-131">string</span></span><br/> | <span data-ttu-id="ce08d-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="ce08d-132">characters</span></span><br/> | <span data-ttu-id="ce08d-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ce08d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ce08d-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ce08d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ce08d-135">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="ce08d-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="ce08d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ce08d-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ce08d-137">string</span><span class="sxs-lookup"><span data-stu-id="ce08d-137">string</span></span><br/> | <span data-ttu-id="ce08d-138">N/D</span><span class="sxs-lookup"><span data-stu-id="ce08d-138">n/a</span></span><br/>        | <span data-ttu-id="ce08d-139">True, False</span><span class="sxs-lookup"><span data-stu-id="ce08d-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="ce08d-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="ce08d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ce08d-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ce08d-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ce08d-142">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="ce08d-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ce08d-143">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="ce08d-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="ce08d-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce08d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce08d-145">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ce08d-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




