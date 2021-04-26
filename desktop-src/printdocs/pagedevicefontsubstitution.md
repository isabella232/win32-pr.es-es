---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f40b86d6d81603e2ff9929275571ff6be72d839b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995592"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="f4819-104">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="f4819-104">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="f4819-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="f4819-105">This topic is not current.</span></span> <span data-ttu-id="f4819-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f4819-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f4819-107">Describe el estado habilitado o deshabilitado de la sustitución de fuentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4819-107">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="f4819-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f4819-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f4819-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="f4819-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f4819-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f4819-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f4819-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f4819-111">Element Information</span></span>



| <span data-ttu-id="f4819-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4819-112">Name</span></span> | <span data-ttu-id="f4819-113">Value</span><span class="sxs-lookup"><span data-stu-id="f4819-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f4819-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f4819-114">Element Type</span></span> <br/>   | <span data-ttu-id="f4819-115">Característica</span><span class="sxs-lookup"><span data-stu-id="f4819-115">Feature</span></span><br/> |
| <span data-ttu-id="f4819-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="f4819-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f4819-117">Página</span><span class="sxs-lookup"><span data-stu-id="f4819-117">Page</span></span><br/>    |
| <span data-ttu-id="f4819-118">Notas</span><span class="sxs-lookup"><span data-stu-id="f4819-118">Notes</span></span> <br/>          | <span data-ttu-id="f4819-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f4819-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f4819-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="f4819-120">Structural Content</span></span>

<span data-ttu-id="f4819-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="f4819-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
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

## <a name="structure-variables"></a><span data-ttu-id="f4819-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="f4819-122">Structure Variables</span></span>

<span data-ttu-id="f4819-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="f4819-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f4819-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4819-124">Name</span></span>                               | <span data-ttu-id="f4819-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f4819-125">Data type</span></span>         | <span data-ttu-id="f4819-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="f4819-126">Unit</span></span>                  | <span data-ttu-id="f4819-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="f4819-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f4819-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="f4819-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f4819-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f4819-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f4819-130">string</span><span class="sxs-lookup"><span data-stu-id="f4819-130">string</span></span><br/> | <span data-ttu-id="f4819-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="f4819-131">characters</span></span><br/> | <span data-ttu-id="f4819-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f4819-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f4819-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f4819-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f4819-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="f4819-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f4819-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f4819-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f4819-136">string</span><span class="sxs-lookup"><span data-stu-id="f4819-136">string</span></span><br/> | <span data-ttu-id="f4819-137">N/D</span><span class="sxs-lookup"><span data-stu-id="f4819-137">n/a</span></span><br/>        | <span data-ttu-id="f4819-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="f4819-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f4819-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="f4819-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f4819-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f4819-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f4819-141">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="f4819-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f4819-142">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="f4819-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Page device font substitution is off -->
  <psf:Option name="psk:Off" />
  <!--Page device font substitution is on -->
  <psf:Option name="psk:On" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="f4819-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4819-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4819-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="f4819-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




