---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: JobPageOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e554da890464afdaed033490def1a915f9d7d800
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105721395"
---
# <a name="jobpageorder"></a><span data-ttu-id="28129-104">JobPageOrder</span><span class="sxs-lookup"><span data-stu-id="28129-104">JobPageOrder</span></span>

<span data-ttu-id="28129-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="28129-105">This topic is not current.</span></span> <span data-ttu-id="28129-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="28129-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="28129-107">Define el orden de las páginas físicas de la salida.</span><span class="sxs-lookup"><span data-stu-id="28129-107">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="28129-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="28129-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="28129-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="28129-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="28129-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="28129-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="28129-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="28129-111">Element Information</span></span>



| <span data-ttu-id="28129-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="28129-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="28129-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="28129-113">Element Type</span></span> <br/>   | <span data-ttu-id="28129-114">Característica</span><span class="sxs-lookup"><span data-stu-id="28129-114">Feature</span></span><br/> |
| <span data-ttu-id="28129-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="28129-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="28129-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="28129-116">Job</span></span><br/>     |
| <span data-ttu-id="28129-117">Notas</span><span class="sxs-lookup"><span data-stu-id="28129-117">Notes</span></span> <br/>          | <span data-ttu-id="28129-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="28129-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="28129-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="28129-119">Structural Content</span></span>

<span data-ttu-id="28129-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="28129-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="28129-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="28129-121">Structure Variables</span></span>

<span data-ttu-id="28129-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="28129-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="28129-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="28129-123">Name</span></span>                               | <span data-ttu-id="28129-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="28129-124">Data type</span></span>         | <span data-ttu-id="28129-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="28129-125">Unit</span></span>                  | <span data-ttu-id="28129-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="28129-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="28129-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="28129-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="28129-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="28129-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="28129-129">string</span><span class="sxs-lookup"><span data-stu-id="28129-129">string</span></span><br/> | <span data-ttu-id="28129-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="28129-130">characters</span></span><br/> | <span data-ttu-id="28129-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="28129-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="28129-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="28129-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="28129-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="28129-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="28129-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="28129-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="28129-135">string</span><span class="sxs-lookup"><span data-stu-id="28129-135">string</span></span><br/> | <span data-ttu-id="28129-136">N/D</span><span class="sxs-lookup"><span data-stu-id="28129-136">n/a</span></span><br/>        | <span data-ttu-id="28129-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="28129-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="28129-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="28129-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="28129-139">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="28129-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="28129-140">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="28129-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="28129-141">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="28129-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="28129-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28129-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28129-143">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="28129-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




