---
description: Revise el elemento configurable por el usuario PageDeviceFontSubstitution. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc5650c687a4c96e6c54ef7ea0631e77407e874
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549203"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="fb725-105">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="fb725-105">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="fb725-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="fb725-106">This topic is not current.</span></span> <span data-ttu-id="fb725-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fb725-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fb725-108">Describe el estado habilitado o deshabilitado de la sustitución de fuentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb725-108">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="fb725-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fb725-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fb725-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="fb725-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fb725-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fb725-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fb725-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fb725-112">Element Information</span></span>



| <span data-ttu-id="fb725-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb725-113">Name</span></span> | <span data-ttu-id="fb725-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fb725-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="fb725-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="fb725-115">Element Type</span></span> <br/>   | <span data-ttu-id="fb725-116">Característica</span><span class="sxs-lookup"><span data-stu-id="fb725-116">Feature</span></span><br/> |
| <span data-ttu-id="fb725-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="fb725-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fb725-118">Página</span><span class="sxs-lookup"><span data-stu-id="fb725-118">Page</span></span><br/>    |
| <span data-ttu-id="fb725-119">Notas</span><span class="sxs-lookup"><span data-stu-id="fb725-119">Notes</span></span> <br/>          | <span data-ttu-id="fb725-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fb725-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="fb725-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="fb725-121">Structural Content</span></span>

<span data-ttu-id="fb725-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="fb725-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="fb725-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="fb725-123">Structure Variables</span></span>

<span data-ttu-id="fb725-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="fb725-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fb725-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb725-125">Name</span></span>                               | <span data-ttu-id="fb725-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fb725-126">Data type</span></span>         | <span data-ttu-id="fb725-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="fb725-127">Unit</span></span>                  | <span data-ttu-id="fb725-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="fb725-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fb725-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="fb725-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fb725-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fb725-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="fb725-131">string</span><span class="sxs-lookup"><span data-stu-id="fb725-131">string</span></span><br/> | <span data-ttu-id="fb725-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="fb725-132">characters</span></span><br/> | <span data-ttu-id="fb725-133">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fb725-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fb725-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fb725-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fb725-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="fb725-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="fb725-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fb725-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="fb725-137">string</span><span class="sxs-lookup"><span data-stu-id="fb725-137">string</span></span><br/> | <span data-ttu-id="fb725-138">N/D</span><span class="sxs-lookup"><span data-stu-id="fb725-138">n/a</span></span><br/>        | <span data-ttu-id="fb725-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="fb725-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fb725-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="fb725-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fb725-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fb725-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fb725-142">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="fb725-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fb725-143">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="fb725-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fb725-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb725-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb725-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="fb725-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




