---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281da67f3f6b90e4e49d0cdc57ba3065d719397b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707647"
---
# <a name="pageposter"></a><span data-ttu-id="c9197-104">PagePoster</span><span class="sxs-lookup"><span data-stu-id="c9197-104">PagePoster</span></span>

<span data-ttu-id="c9197-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="c9197-105">This topic is not current.</span></span> <span data-ttu-id="c9197-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c9197-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c9197-107">Describe el resultado de una sola página en varias hojas de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="c9197-107">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="c9197-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c9197-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c9197-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c9197-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c9197-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c9197-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c9197-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c9197-111">Element Information</span></span>



| <span data-ttu-id="c9197-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9197-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="c9197-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c9197-113">Element Type</span></span> <br/>   | <span data-ttu-id="c9197-114">Característica</span><span class="sxs-lookup"><span data-stu-id="c9197-114">Feature</span></span><br/> |
| <span data-ttu-id="c9197-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="c9197-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c9197-116">Página</span><span class="sxs-lookup"><span data-stu-id="c9197-116">Page</span></span><br/>    |
| <span data-ttu-id="c9197-117">Notas</span><span class="sxs-lookup"><span data-stu-id="c9197-117">Notes</span></span> <br/>          | <span data-ttu-id="c9197-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c9197-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c9197-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c9197-119">Structural Content</span></span>

<span data-ttu-id="c9197-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="c9197-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c9197-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="c9197-121">Structure Variables</span></span>

<span data-ttu-id="c9197-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="c9197-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c9197-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9197-123">Name</span></span>                               | <span data-ttu-id="c9197-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c9197-124">Data type</span></span>          | <span data-ttu-id="c9197-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="c9197-125">Unit</span></span>                  | <span data-ttu-id="c9197-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="c9197-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c9197-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="c9197-127">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c9197-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c9197-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c9197-129">string</span><span class="sxs-lookup"><span data-stu-id="c9197-129">string</span></span><br/>  | <span data-ttu-id="c9197-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="c9197-130">characters</span></span><br/> | <span data-ttu-id="c9197-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c9197-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c9197-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c9197-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c9197-133">El nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="c9197-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="c9197-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c9197-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c9197-135">string</span><span class="sxs-lookup"><span data-stu-id="c9197-135">string</span></span><br/>  | <span data-ttu-id="c9197-136">N/D</span><span class="sxs-lookup"><span data-stu-id="c9197-136">n/a</span></span><br/>        | <span data-ttu-id="c9197-137">True, False</span><span class="sxs-lookup"><span data-stu-id="c9197-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="c9197-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="c9197-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="c9197-139">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="c9197-139">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="c9197-140">integer</span><span class="sxs-lookup"><span data-stu-id="c9197-140">integer</span></span><br/> | <span data-ttu-id="c9197-141">páginas</span><span class="sxs-lookup"><span data-stu-id="c9197-141">pages</span></span><br/>      | <span data-ttu-id="c9197-142">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="c9197-142">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="c9197-143">Especifica el número de hojas físicas por página lógica.</span><span class="sxs-lookup"><span data-stu-id="c9197-143">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c9197-144">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c9197-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c9197-145">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c9197-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c9197-146">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="c9197-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c9197-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9197-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9197-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c9197-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




