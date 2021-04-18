---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: PageBorderless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd73e2808380bf73a7df7156c10c40cfa339765
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707634"
---
# <a name="pageborderless"></a><span data-ttu-id="9bf22-104">PageBorderless</span><span class="sxs-lookup"><span data-stu-id="9bf22-104">PageBorderless</span></span>

<span data-ttu-id="9bf22-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="9bf22-105">This topic is not current.</span></span> <span data-ttu-id="9bf22-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9bf22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9bf22-107">Describe cuándo se debe imprimir el contenido de la imagen en los bordes físicos del medio.</span><span class="sxs-lookup"><span data-stu-id="9bf22-107">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="9bf22-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9bf22-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9bf22-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9bf22-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9bf22-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="9bf22-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9bf22-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9bf22-111">Element Information</span></span>



| <span data-ttu-id="9bf22-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bf22-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="9bf22-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9bf22-113">Element Type</span></span> <br/>   | <span data-ttu-id="9bf22-114">Característica</span><span class="sxs-lookup"><span data-stu-id="9bf22-114">Feature</span></span><br/> |
| <span data-ttu-id="9bf22-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9bf22-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9bf22-116">Página</span><span class="sxs-lookup"><span data-stu-id="9bf22-116">Page</span></span><br/>    |
| <span data-ttu-id="9bf22-117">Notas</span><span class="sxs-lookup"><span data-stu-id="9bf22-117">Notes</span></span> <br/>          | <span data-ttu-id="9bf22-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9bf22-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9bf22-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9bf22-119">Structural Content</span></span>

<span data-ttu-id="9bf22-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9bf22-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
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

## <a name="structure-variables"></a><span data-ttu-id="9bf22-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9bf22-121">Structure Variables</span></span>

<span data-ttu-id="9bf22-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9bf22-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9bf22-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bf22-123">Name</span></span>                               | <span data-ttu-id="9bf22-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9bf22-124">Data type</span></span>         | <span data-ttu-id="9bf22-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="9bf22-125">Unit</span></span>                  | <span data-ttu-id="9bf22-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9bf22-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9bf22-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="9bf22-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9bf22-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9bf22-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9bf22-129">string</span><span class="sxs-lookup"><span data-stu-id="9bf22-129">string</span></span><br/> | <span data-ttu-id="9bf22-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="9bf22-130">characters</span></span><br/> | <span data-ttu-id="9bf22-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9bf22-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9bf22-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9bf22-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9bf22-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9bf22-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9bf22-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9bf22-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9bf22-135">string</span><span class="sxs-lookup"><span data-stu-id="9bf22-135">string</span></span><br/> | <span data-ttu-id="9bf22-136">N/D</span><span class="sxs-lookup"><span data-stu-id="9bf22-136">n/a</span></span><br/>        | <span data-ttu-id="9bf22-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="9bf22-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9bf22-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9bf22-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9bf22-139">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="9bf22-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9bf22-140">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9bf22-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9bf22-141">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9bf22-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies borderless printing. -->
  <psf:Option name="psk:Borderless" />
  <!-- Specifies no borderless printing. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9bf22-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bf22-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf22-143">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9bf22-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




