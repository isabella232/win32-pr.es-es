---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c63238c290d6b8f0bb208e94e52dc66c8d2e6be
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994482"
---
# <a name="pageoutputquality"></a><span data-ttu-id="35fd4-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="35fd4-104">PageOutputQuality</span></span>

<span data-ttu-id="35fd4-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="35fd4-105">This topic is not current.</span></span> <span data-ttu-id="35fd4-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="35fd4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="35fd4-107">Describe el nivel de calidad de la salida.</span><span class="sxs-lookup"><span data-stu-id="35fd4-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="35fd4-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="35fd4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="35fd4-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="35fd4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="35fd4-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="35fd4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="35fd4-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="35fd4-111">Element Information</span></span>



| <span data-ttu-id="35fd4-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="35fd4-112">Name</span></span> | <span data-ttu-id="35fd4-113">Value</span><span class="sxs-lookup"><span data-stu-id="35fd4-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="35fd4-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="35fd4-114">Element Type</span></span> <br/>   | <span data-ttu-id="35fd4-115">Característica</span><span class="sxs-lookup"><span data-stu-id="35fd4-115">Feature</span></span><br/> |
| <span data-ttu-id="35fd4-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="35fd4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="35fd4-117">Página</span><span class="sxs-lookup"><span data-stu-id="35fd4-117">Page</span></span><br/>    |
| <span data-ttu-id="35fd4-118">Notas</span><span class="sxs-lookup"><span data-stu-id="35fd4-118">Notes</span></span> <br/>          | <span data-ttu-id="35fd4-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="35fd4-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="35fd4-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="35fd4-120">Structural Content</span></span>

<span data-ttu-id="35fd4-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="35fd4-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="35fd4-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="35fd4-122">Structure Variables</span></span>

<span data-ttu-id="35fd4-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="35fd4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="35fd4-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="35fd4-124">Name</span></span>                               | <span data-ttu-id="35fd4-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="35fd4-125">Data type</span></span>         | <span data-ttu-id="35fd4-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="35fd4-126">Unit</span></span>                  | <span data-ttu-id="35fd4-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="35fd4-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="35fd4-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="35fd4-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="35fd4-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="35fd4-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="35fd4-130">string</span><span class="sxs-lookup"><span data-stu-id="35fd4-130">string</span></span><br/> | <span data-ttu-id="35fd4-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="35fd4-131">characters</span></span><br/> | <span data-ttu-id="35fd4-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="35fd4-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="35fd4-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35fd4-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="35fd4-134">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="35fd4-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="35fd4-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="35fd4-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="35fd4-136">string</span><span class="sxs-lookup"><span data-stu-id="35fd4-136">string</span></span><br/> | <span data-ttu-id="35fd4-137">N/D</span><span class="sxs-lookup"><span data-stu-id="35fd4-137">n/a</span></span><br/>        | <span data-ttu-id="35fd4-138">True, False</span><span class="sxs-lookup"><span data-stu-id="35fd4-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="35fd4-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="35fd4-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="35fd4-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="35fd4-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="35fd4-141">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="35fd4-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="35fd4-142">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="35fd4-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="35fd4-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35fd4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35fd4-144">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="35fd4-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




