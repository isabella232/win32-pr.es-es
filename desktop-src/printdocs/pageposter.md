---
description: Obtenga información sobre el elemento configurable por el usuario PagePoster. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548973"
---
# <a name="pageposter"></a><span data-ttu-id="25266-105">PagePoster</span><span class="sxs-lookup"><span data-stu-id="25266-105">PagePoster</span></span>

<span data-ttu-id="25266-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="25266-106">This topic is not current.</span></span> <span data-ttu-id="25266-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="25266-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="25266-108">Describe la salida de una sola página a varias hojas de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="25266-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="25266-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="25266-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="25266-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="25266-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="25266-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="25266-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="25266-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="25266-112">Element Information</span></span>



| <span data-ttu-id="25266-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="25266-113">Name</span></span> | <span data-ttu-id="25266-114">Valor</span><span class="sxs-lookup"><span data-stu-id="25266-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="25266-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="25266-115">Element Type</span></span> <br/>   | <span data-ttu-id="25266-116">Característica</span><span class="sxs-lookup"><span data-stu-id="25266-116">Feature</span></span><br/> |
| <span data-ttu-id="25266-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="25266-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="25266-118">Página</span><span class="sxs-lookup"><span data-stu-id="25266-118">Page</span></span><br/>    |
| <span data-ttu-id="25266-119">Notas</span><span class="sxs-lookup"><span data-stu-id="25266-119">Notes</span></span> <br/>          | <span data-ttu-id="25266-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="25266-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="25266-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="25266-121">Structural Content</span></span>

<span data-ttu-id="25266-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="25266-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="25266-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="25266-123">Structure Variables</span></span>

<span data-ttu-id="25266-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="25266-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="25266-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="25266-125">Name</span></span>                               | <span data-ttu-id="25266-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="25266-126">Data type</span></span>          | <span data-ttu-id="25266-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="25266-127">Unit</span></span>                  | <span data-ttu-id="25266-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="25266-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="25266-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="25266-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="25266-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="25266-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="25266-131">string</span><span class="sxs-lookup"><span data-stu-id="25266-131">string</span></span><br/>  | <span data-ttu-id="25266-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="25266-132">characters</span></span><br/> | <span data-ttu-id="25266-133">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="25266-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="25266-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="25266-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="25266-135">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="25266-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="25266-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="25266-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="25266-137">string</span><span class="sxs-lookup"><span data-stu-id="25266-137">string</span></span><br/>  | <span data-ttu-id="25266-138">N/D</span><span class="sxs-lookup"><span data-stu-id="25266-138">n/a</span></span><br/>        | <span data-ttu-id="25266-139">True, False</span><span class="sxs-lookup"><span data-stu-id="25266-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="25266-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="25266-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="25266-141">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="25266-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="25266-142">integer</span><span class="sxs-lookup"><span data-stu-id="25266-142">integer</span></span><br/> | <span data-ttu-id="25266-143">páginas</span><span class="sxs-lookup"><span data-stu-id="25266-143">pages</span></span><br/>      | <span data-ttu-id="25266-144">Mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="25266-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="25266-145">Especifica el número de hojas físicas por página lógica.</span><span class="sxs-lookup"><span data-stu-id="25266-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="25266-146">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="25266-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="25266-147">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="25266-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="25266-148">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="25266-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="25266-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25266-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25266-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="25266-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




