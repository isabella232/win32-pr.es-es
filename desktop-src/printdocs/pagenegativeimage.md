---
description: Obtenga información sobre el elemento configurable por el usuario PageNegativeImage. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1e1a9de2d82135adb82c68f45785ee3763e41a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395660"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="aeff0-105">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="aeff0-105">PageNegativeImage</span></span>

<span data-ttu-id="aeff0-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="aeff0-106">This topic is not current.</span></span> <span data-ttu-id="aeff0-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aeff0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aeff0-108">Describe la configuración negativa de la salida.</span><span class="sxs-lookup"><span data-stu-id="aeff0-108">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="aeff0-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="aeff0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aeff0-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="aeff0-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="aeff0-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="aeff0-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aeff0-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="aeff0-112">Element Information</span></span>



| <span data-ttu-id="aeff0-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="aeff0-113">Name</span></span> | <span data-ttu-id="aeff0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="aeff0-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="aeff0-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="aeff0-115">Element Type</span></span> <br/>   | <span data-ttu-id="aeff0-116">Característica</span><span class="sxs-lookup"><span data-stu-id="aeff0-116">Feature</span></span><br/> |
| <span data-ttu-id="aeff0-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="aeff0-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aeff0-118">Página</span><span class="sxs-lookup"><span data-stu-id="aeff0-118">Page</span></span><br/>    |
| <span data-ttu-id="aeff0-119">Notas</span><span class="sxs-lookup"><span data-stu-id="aeff0-119">Notes</span></span> <br/>          | <span data-ttu-id="aeff0-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aeff0-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="aeff0-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="aeff0-121">Structural Content</span></span>

<span data-ttu-id="aeff0-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="aeff0-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
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

## <a name="structure-variables"></a><span data-ttu-id="aeff0-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="aeff0-123">Structure Variables</span></span>

<span data-ttu-id="aeff0-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="aeff0-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aeff0-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="aeff0-125">Name</span></span>                               | <span data-ttu-id="aeff0-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aeff0-126">Data type</span></span>         | <span data-ttu-id="aeff0-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="aeff0-127">Unit</span></span>                  | <span data-ttu-id="aeff0-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="aeff0-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="aeff0-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="aeff0-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aeff0-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="aeff0-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="aeff0-131">string</span><span class="sxs-lookup"><span data-stu-id="aeff0-131">string</span></span><br/> | <span data-ttu-id="aeff0-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="aeff0-132">characters</span></span><br/> | <span data-ttu-id="aeff0-133">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="aeff0-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="aeff0-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aeff0-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aeff0-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="aeff0-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="aeff0-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="aeff0-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="aeff0-137">string</span><span class="sxs-lookup"><span data-stu-id="aeff0-137">string</span></span><br/> | <span data-ttu-id="aeff0-138">N/D</span><span class="sxs-lookup"><span data-stu-id="aeff0-138">n/a</span></span><br/>        | <span data-ttu-id="aeff0-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="aeff0-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="aeff0-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="aeff0-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aeff0-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="aeff0-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aeff0-142">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="aeff0-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aeff0-143">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="aeff0-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="aeff0-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aeff0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeff0-145">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="aeff0-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




