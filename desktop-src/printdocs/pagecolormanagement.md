---
description: Obtenga información sobre el elemento configurable por el usuario PageColorManagement. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549233"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="570a4-105">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="570a4-105">PageColorManagement</span></span>

<span data-ttu-id="570a4-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="570a4-106">This topic is not current.</span></span> <span data-ttu-id="570a4-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="570a4-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="570a4-108">Configura la administración de colores para la página actual.</span><span class="sxs-lookup"><span data-stu-id="570a4-108">Configures color management for the current page.</span></span> <span data-ttu-id="570a4-109">Esto se considera automático en SHIM: DM \_ ICMMethod Agregar sistema.</span><span class="sxs-lookup"><span data-stu-id="570a4-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="570a4-110">Describe qué componente debe realizar la administración de colores (es decir, controlador).</span><span class="sxs-lookup"><span data-stu-id="570a4-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="570a4-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="570a4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="570a4-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="570a4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="570a4-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="570a4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="570a4-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="570a4-114">Element Information</span></span>



| <span data-ttu-id="570a4-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="570a4-115">Name</span></span> | <span data-ttu-id="570a4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="570a4-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="570a4-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="570a4-117">Element Type</span></span> <br/>   | <span data-ttu-id="570a4-118">Característica</span><span class="sxs-lookup"><span data-stu-id="570a4-118">Feature</span></span><br/> |
| <span data-ttu-id="570a4-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="570a4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="570a4-120">Página</span><span class="sxs-lookup"><span data-stu-id="570a4-120">Page</span></span><br/>    |
| <span data-ttu-id="570a4-121">Notas</span><span class="sxs-lookup"><span data-stu-id="570a4-121">Notes</span></span> <br/>          | <span data-ttu-id="570a4-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="570a4-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="570a4-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="570a4-123">Structural Content</span></span>

<span data-ttu-id="570a4-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="570a4-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="570a4-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="570a4-125">Structure Variables</span></span>

<span data-ttu-id="570a4-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="570a4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="570a4-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="570a4-127">Name</span></span>                               | <span data-ttu-id="570a4-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="570a4-128">Data type</span></span>         | <span data-ttu-id="570a4-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="570a4-129">Unit</span></span>                  | <span data-ttu-id="570a4-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="570a4-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="570a4-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="570a4-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="570a4-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="570a4-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="570a4-133">string</span><span class="sxs-lookup"><span data-stu-id="570a4-133">string</span></span><br/> | <span data-ttu-id="570a4-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="570a4-134">characters</span></span><br/> | <span data-ttu-id="570a4-135">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="570a4-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="570a4-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="570a4-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="570a4-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="570a4-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="570a4-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="570a4-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="570a4-139">string</span><span class="sxs-lookup"><span data-stu-id="570a4-139">string</span></span><br/> | <span data-ttu-id="570a4-140">N/D</span><span class="sxs-lookup"><span data-stu-id="570a4-140">n/a</span></span><br/>        | <span data-ttu-id="570a4-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="570a4-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="570a4-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="570a4-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="570a4-143">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="570a4-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="570a4-144">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="570a4-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="570a4-145">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="570a4-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="570a4-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="570a4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="570a4-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="570a4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




