---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81a037b6b32ff71b53688dfd6fc8afd5f10bb69
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997662"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="5ae42-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="5ae42-104">PageColorManagement</span></span>

<span data-ttu-id="5ae42-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5ae42-105">This topic is not current.</span></span> <span data-ttu-id="5ae42-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5ae42-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ae42-107">Configura la administración de colores para la página actual.</span><span class="sxs-lookup"><span data-stu-id="5ae42-107">Configures color management for the current page.</span></span> <span data-ttu-id="5ae42-108">Esto se considera automático en SHIM: DM \_ ICMMethod Add System.</span><span class="sxs-lookup"><span data-stu-id="5ae42-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="5ae42-109">Describe qué componente debe realizar la administración de colores (es decir, controlador).</span><span class="sxs-lookup"><span data-stu-id="5ae42-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="5ae42-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5ae42-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5ae42-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="5ae42-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5ae42-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5ae42-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5ae42-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5ae42-113">Element Information</span></span>



| <span data-ttu-id="5ae42-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ae42-114">Name</span></span> | <span data-ttu-id="5ae42-115">Value</span><span class="sxs-lookup"><span data-stu-id="5ae42-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5ae42-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5ae42-116">Element Type</span></span> <br/>   | <span data-ttu-id="5ae42-117">Característica</span><span class="sxs-lookup"><span data-stu-id="5ae42-117">Feature</span></span><br/> |
| <span data-ttu-id="5ae42-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5ae42-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5ae42-119">Página</span><span class="sxs-lookup"><span data-stu-id="5ae42-119">Page</span></span><br/>    |
| <span data-ttu-id="5ae42-120">Notas</span><span class="sxs-lookup"><span data-stu-id="5ae42-120">Notes</span></span> <br/>          | <span data-ttu-id="5ae42-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5ae42-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="5ae42-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="5ae42-122">Structural Content</span></span>

<span data-ttu-id="5ae42-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5ae42-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="5ae42-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="5ae42-124">Structure Variables</span></span>

<span data-ttu-id="5ae42-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5ae42-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5ae42-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ae42-126">Name</span></span>                               | <span data-ttu-id="5ae42-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5ae42-127">Data type</span></span>         | <span data-ttu-id="5ae42-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="5ae42-128">Unit</span></span>                  | <span data-ttu-id="5ae42-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="5ae42-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5ae42-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="5ae42-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5ae42-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5ae42-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5ae42-132">string</span><span class="sxs-lookup"><span data-stu-id="5ae42-132">string</span></span><br/> | <span data-ttu-id="5ae42-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="5ae42-133">characters</span></span><br/> | <span data-ttu-id="5ae42-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5ae42-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5ae42-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5ae42-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5ae42-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="5ae42-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5ae42-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5ae42-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5ae42-138">string</span><span class="sxs-lookup"><span data-stu-id="5ae42-138">string</span></span><br/> | <span data-ttu-id="5ae42-139">N/D</span><span class="sxs-lookup"><span data-stu-id="5ae42-139">n/a</span></span><br/>        | <span data-ttu-id="5ae42-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="5ae42-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5ae42-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="5ae42-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5ae42-142">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5ae42-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5ae42-143">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="5ae42-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5ae42-144">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="5ae42-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5ae42-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ae42-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae42-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5ae42-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




