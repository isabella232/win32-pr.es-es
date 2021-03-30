---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279909"
---
# <a name="documentduplex"></a><span data-ttu-id="75c37-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="75c37-104">DocumentDuplex</span></span>

<span data-ttu-id="75c37-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="75c37-105">This topic is not current.</span></span> <span data-ttu-id="75c37-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="75c37-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75c37-107">Describe las características dúplex de la salida.</span><span class="sxs-lookup"><span data-stu-id="75c37-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="75c37-108">La característica dúplex permite la impresión en ambos lados del medio.</span><span class="sxs-lookup"><span data-stu-id="75c37-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="75c37-109">Cada documento está dúplex por separado.</span><span class="sxs-lookup"><span data-stu-id="75c37-109">Each document is duplexed separately.</span></span> <span data-ttu-id="75c37-110">DocumentDuplex y JobDuplexAllDocumentsContiguously se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="75c37-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="75c37-111">Es el controlador el que determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="75c37-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="75c37-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="75c37-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75c37-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="75c37-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="75c37-114">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="75c37-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="75c37-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="75c37-115">Element Information</span></span>



| <span data-ttu-id="75c37-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="75c37-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="75c37-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="75c37-117">Element Type</span></span> <br/>   | <span data-ttu-id="75c37-118">Característica</span><span class="sxs-lookup"><span data-stu-id="75c37-118">Feature</span></span><br/>  |
| <span data-ttu-id="75c37-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="75c37-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75c37-120">Documento</span><span class="sxs-lookup"><span data-stu-id="75c37-120">Document</span></span><br/> |
| <span data-ttu-id="75c37-121">Notas</span><span class="sxs-lookup"><span data-stu-id="75c37-121">Notes</span></span> <br/>          | <span data-ttu-id="75c37-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="75c37-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="75c37-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="75c37-123">Structural Content</span></span>

<span data-ttu-id="75c37-124">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="75c37-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="75c37-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="75c37-125">Structure Variables</span></span>

<span data-ttu-id="75c37-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="75c37-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75c37-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="75c37-127">Name</span></span>                               | <span data-ttu-id="75c37-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="75c37-128">Data type</span></span>         | <span data-ttu-id="75c37-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="75c37-129">Unit</span></span>                  | <span data-ttu-id="75c37-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="75c37-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="75c37-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="75c37-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c37-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="75c37-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="75c37-133">string</span><span class="sxs-lookup"><span data-stu-id="75c37-133">string</span></span><br/> | <span data-ttu-id="75c37-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="75c37-134">characters</span></span><br/> | <span data-ttu-id="75c37-135">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="75c37-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="75c37-136">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="75c37-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="75c37-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="75c37-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="75c37-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75c37-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="75c37-139">string</span><span class="sxs-lookup"><span data-stu-id="75c37-139">string</span></span><br/> | <span data-ttu-id="75c37-140">N/D</span><span class="sxs-lookup"><span data-stu-id="75c37-140">n/a</span></span><br/>        | <span data-ttu-id="75c37-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="75c37-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75c37-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="75c37-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="75c37-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="75c37-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="75c37-144">string</span><span class="sxs-lookup"><span data-stu-id="75c37-144">string</span></span><br/> | <span data-ttu-id="75c37-145">N/D</span><span class="sxs-lookup"><span data-stu-id="75c37-145">n/a</span></span><br/>        | <span data-ttu-id="75c37-146">Automática, manual.</span><span class="sxs-lookup"><span data-stu-id="75c37-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="75c37-147">Define el modo dúplex.</span><span class="sxs-lookup"><span data-stu-id="75c37-147">Defines the duplex mode.</span></span> <span data-ttu-id="75c37-148">El hardware automático realiza la operación dúplex automática.</span><span class="sxs-lookup"><span data-stu-id="75c37-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="75c37-149">El software y el usuario realizan la función de dúplex manual.</span><span class="sxs-lookup"><span data-stu-id="75c37-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="75c37-150">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="75c37-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="75c37-151">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="75c37-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="75c37-152">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="75c37-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="75c37-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75c37-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c37-154">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="75c37-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




