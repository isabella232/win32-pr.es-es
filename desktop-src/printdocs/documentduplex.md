---
description: Obtenga información sobre el elemento DocumentDuplex, que describe las características dúplex de la salida. La característica dúplex permite imprimir en ambos lados del medio.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ad8521835213594f10507ab6fd4b9cca24040
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409348"
---
# <a name="documentduplex"></a><span data-ttu-id="705e6-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="705e6-104">DocumentDuplex</span></span>

<span data-ttu-id="705e6-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="705e6-105">This topic is not current.</span></span> <span data-ttu-id="705e6-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="705e6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="705e6-107">Describe las características dúplex de la salida.</span><span class="sxs-lookup"><span data-stu-id="705e6-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="705e6-108">La característica dúplex permite imprimir en ambos lados del medio.</span><span class="sxs-lookup"><span data-stu-id="705e6-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="705e6-109">Cada documento se dúplex por separado.</span><span class="sxs-lookup"><span data-stu-id="705e6-109">Each document is duplexed separately.</span></span> <span data-ttu-id="705e6-110">DocumentDuplex y JobDuplexAllDocumentsContiguously son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="705e6-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="705e6-111">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="705e6-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="705e6-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="705e6-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="705e6-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="705e6-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="705e6-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="705e6-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="705e6-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="705e6-115">Element Information</span></span>



| <span data-ttu-id="705e6-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="705e6-116">Name</span></span> | <span data-ttu-id="705e6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="705e6-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="705e6-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="705e6-118">Element Type</span></span> <br/>   | <span data-ttu-id="705e6-119">Característica</span><span class="sxs-lookup"><span data-stu-id="705e6-119">Feature</span></span><br/>  |
| <span data-ttu-id="705e6-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="705e6-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="705e6-121">Documento</span><span class="sxs-lookup"><span data-stu-id="705e6-121">Document</span></span><br/> |
| <span data-ttu-id="705e6-122">Notas</span><span class="sxs-lookup"><span data-stu-id="705e6-122">Notes</span></span> <br/>          | <span data-ttu-id="705e6-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="705e6-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="705e6-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="705e6-124">Structural Content</span></span>

<span data-ttu-id="705e6-125">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="705e6-125">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="705e6-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="705e6-126">Structure Variables</span></span>

<span data-ttu-id="705e6-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="705e6-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="705e6-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="705e6-128">Name</span></span>                               | <span data-ttu-id="705e6-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="705e6-129">Data type</span></span>         | <span data-ttu-id="705e6-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="705e6-130">Unit</span></span>                  | <span data-ttu-id="705e6-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="705e6-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="705e6-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="705e6-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705e6-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="705e6-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="705e6-134">string</span><span class="sxs-lookup"><span data-stu-id="705e6-134">string</span></span><br/> | <span data-ttu-id="705e6-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="705e6-135">characters</span></span><br/> | <span data-ttu-id="705e6-136">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="705e6-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="705e6-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="705e6-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="705e6-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="705e6-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="705e6-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="705e6-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="705e6-140">string</span><span class="sxs-lookup"><span data-stu-id="705e6-140">string</span></span><br/> | <span data-ttu-id="705e6-141">N/D</span><span class="sxs-lookup"><span data-stu-id="705e6-141">n/a</span></span><br/>        | <span data-ttu-id="705e6-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="705e6-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="705e6-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="705e6-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="705e6-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="705e6-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="705e6-145">string</span><span class="sxs-lookup"><span data-stu-id="705e6-145">string</span></span><br/> | <span data-ttu-id="705e6-146">N/D</span><span class="sxs-lookup"><span data-stu-id="705e6-146">n/a</span></span><br/>        | <span data-ttu-id="705e6-147">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="705e6-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="705e6-148">Define el modo dúplex.</span><span class="sxs-lookup"><span data-stu-id="705e6-148">Defines the duplex mode.</span></span> <span data-ttu-id="705e6-149">El dúplex automático lo realiza el hardware.</span><span class="sxs-lookup"><span data-stu-id="705e6-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="705e6-150">El software y el usuario realizan el dúplex manual.</span><span class="sxs-lookup"><span data-stu-id="705e6-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="705e6-151">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="705e6-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="705e6-152">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="705e6-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="705e6-153">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="705e6-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="705e6-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="705e6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="705e6-155">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="705e6-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




