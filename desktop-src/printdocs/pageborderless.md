---
description: Obtenga información sobre el elemento PageBorderless configurable por el usuario. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: PageBorderless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a0ff13edc1f4e5b36f55229559bb06ed17150b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549313"
---
# <a name="pageborderless"></a><span data-ttu-id="90de9-105">PageBorderless</span><span class="sxs-lookup"><span data-stu-id="90de9-105">PageBorderless</span></span>

<span data-ttu-id="90de9-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="90de9-106">This topic is not current.</span></span> <span data-ttu-id="90de9-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="90de9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="90de9-108">Describe cuándo se debe imprimir el contenido de la imagen en los bordes físicos del medio.</span><span class="sxs-lookup"><span data-stu-id="90de9-108">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="90de9-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="90de9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="90de9-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="90de9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="90de9-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="90de9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="90de9-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="90de9-112">Element Information</span></span>



| <span data-ttu-id="90de9-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="90de9-113">Name</span></span> | <span data-ttu-id="90de9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="90de9-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="90de9-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="90de9-115">Element Type</span></span> <br/>   | <span data-ttu-id="90de9-116">Característica</span><span class="sxs-lookup"><span data-stu-id="90de9-116">Feature</span></span><br/> |
| <span data-ttu-id="90de9-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="90de9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="90de9-118">Página</span><span class="sxs-lookup"><span data-stu-id="90de9-118">Page</span></span><br/>    |
| <span data-ttu-id="90de9-119">Notas</span><span class="sxs-lookup"><span data-stu-id="90de9-119">Notes</span></span> <br/>          | <span data-ttu-id="90de9-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="90de9-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="90de9-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="90de9-121">Structural Content</span></span>

<span data-ttu-id="90de9-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="90de9-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="90de9-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="90de9-123">Structure Variables</span></span>

<span data-ttu-id="90de9-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="90de9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="90de9-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="90de9-125">Name</span></span>                               | <span data-ttu-id="90de9-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="90de9-126">Data type</span></span>         | <span data-ttu-id="90de9-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="90de9-127">Unit</span></span>                  | <span data-ttu-id="90de9-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="90de9-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="90de9-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="90de9-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="90de9-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="90de9-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="90de9-131">string</span><span class="sxs-lookup"><span data-stu-id="90de9-131">string</span></span><br/> | <span data-ttu-id="90de9-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="90de9-132">characters</span></span><br/> | <span data-ttu-id="90de9-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="90de9-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="90de9-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="90de9-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="90de9-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="90de9-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="90de9-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="90de9-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="90de9-137">string</span><span class="sxs-lookup"><span data-stu-id="90de9-137">string</span></span><br/> | <span data-ttu-id="90de9-138">N/D</span><span class="sxs-lookup"><span data-stu-id="90de9-138">n/a</span></span><br/>        | <span data-ttu-id="90de9-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="90de9-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="90de9-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="90de9-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="90de9-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="90de9-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="90de9-142">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="90de9-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="90de9-143">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="90de9-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="90de9-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90de9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90de9-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="90de9-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




