---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707640"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="8b944-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="8b944-104">PageColorManagement</span></span>

<span data-ttu-id="8b944-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="8b944-105">This topic is not current.</span></span> <span data-ttu-id="8b944-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8b944-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8b944-107">Configura la administración del color de la página actual.</span><span class="sxs-lookup"><span data-stu-id="8b944-107">Configures color management for the current page.</span></span> <span data-ttu-id="8b944-108">Esto se considera automático en SHIM-DM \_ ICMMethod agregar sistema.</span><span class="sxs-lookup"><span data-stu-id="8b944-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="8b944-109">Describe qué componente debe llevar a cabo la administración del color (es decir, el controlador).</span><span class="sxs-lookup"><span data-stu-id="8b944-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="8b944-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8b944-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8b944-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="8b944-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8b944-112">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="8b944-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8b944-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8b944-113">Element Information</span></span>



| <span data-ttu-id="8b944-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="8b944-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="8b944-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8b944-115">Element Type</span></span> <br/>   | <span data-ttu-id="8b944-116">Característica</span><span class="sxs-lookup"><span data-stu-id="8b944-116">Feature</span></span><br/> |
| <span data-ttu-id="8b944-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="8b944-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8b944-118">Página</span><span class="sxs-lookup"><span data-stu-id="8b944-118">Page</span></span><br/>    |
| <span data-ttu-id="8b944-119">Notas</span><span class="sxs-lookup"><span data-stu-id="8b944-119">Notes</span></span> <br/>          | <span data-ttu-id="8b944-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8b944-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="8b944-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="8b944-121">Structural Content</span></span>

<span data-ttu-id="8b944-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="8b944-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8b944-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="8b944-123">Structure Variables</span></span>

<span data-ttu-id="8b944-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="8b944-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8b944-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="8b944-125">Name</span></span>                               | <span data-ttu-id="8b944-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8b944-126">Data type</span></span>         | <span data-ttu-id="8b944-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="8b944-127">Unit</span></span>                  | <span data-ttu-id="8b944-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="8b944-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8b944-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="8b944-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8b944-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8b944-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8b944-131">string</span><span class="sxs-lookup"><span data-stu-id="8b944-131">string</span></span><br/> | <span data-ttu-id="8b944-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="8b944-132">characters</span></span><br/> | <span data-ttu-id="8b944-133">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8b944-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8b944-134">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8b944-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8b944-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="8b944-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8b944-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8b944-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8b944-137">string</span><span class="sxs-lookup"><span data-stu-id="8b944-137">string</span></span><br/> | <span data-ttu-id="8b944-138">N/D</span><span class="sxs-lookup"><span data-stu-id="8b944-138">n/a</span></span><br/>        | <span data-ttu-id="8b944-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="8b944-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8b944-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="8b944-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8b944-141">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="8b944-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8b944-142">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8b944-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8b944-143">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="8b944-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8b944-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b944-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b944-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8b944-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




