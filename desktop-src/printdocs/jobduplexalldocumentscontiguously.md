---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c14e9c536d0ab24fafe308a8b11fa769842aab
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707632"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="45c6c-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="45c6c-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="45c6c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="45c6c-105">This topic is not current.</span></span> <span data-ttu-id="45c6c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="45c6c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="45c6c-107">Describe las características dúplex de la salida.</span><span class="sxs-lookup"><span data-stu-id="45c6c-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="45c6c-108">La característica dúplex permite la impresión en ambos lados del medio.</span><span class="sxs-lookup"><span data-stu-id="45c6c-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="45c6c-109">Todos los documentos del trabajo están Dúplexs juntos de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="45c6c-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="45c6c-110">JobDuplexAllDocumentsContiguously y DocumentDuplex se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="45c6c-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="45c6c-111">Es el controlador el que determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="45c6c-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="45c6c-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="45c6c-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="45c6c-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="45c6c-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="45c6c-114">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="45c6c-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="45c6c-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="45c6c-115">Element Information</span></span>



| <span data-ttu-id="45c6c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="45c6c-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="45c6c-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="45c6c-117">Element Type</span></span> <br/>   | <span data-ttu-id="45c6c-118">Característica</span><span class="sxs-lookup"><span data-stu-id="45c6c-118">Feature</span></span><br/> |
| <span data-ttu-id="45c6c-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="45c6c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="45c6c-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="45c6c-120">Job</span></span><br/>     |
| <span data-ttu-id="45c6c-121">Notas</span><span class="sxs-lookup"><span data-stu-id="45c6c-121">Notes</span></span> <br/>          | <span data-ttu-id="45c6c-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="45c6c-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="45c6c-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="45c6c-123">Structural Content</span></span>

<span data-ttu-id="45c6c-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="45c6c-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
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

## <a name="structure-variables"></a><span data-ttu-id="45c6c-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="45c6c-125">Structure Variables</span></span>

<span data-ttu-id="45c6c-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="45c6c-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="45c6c-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="45c6c-127">Name</span></span>                               | <span data-ttu-id="45c6c-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="45c6c-128">Data type</span></span>         | <span data-ttu-id="45c6c-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="45c6c-129">Unit</span></span>                  | <span data-ttu-id="45c6c-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="45c6c-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="45c6c-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="45c6c-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c6c-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="45c6c-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="45c6c-133">string</span><span class="sxs-lookup"><span data-stu-id="45c6c-133">string</span></span><br/> | <span data-ttu-id="45c6c-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="45c6c-134">characters</span></span><br/> | <span data-ttu-id="45c6c-135">Nombre completo válido, tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="45c6c-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="45c6c-136">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="45c6c-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="45c6c-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="45c6c-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="45c6c-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="45c6c-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="45c6c-139">string</span><span class="sxs-lookup"><span data-stu-id="45c6c-139">string</span></span><br/> | <span data-ttu-id="45c6c-140">N/D</span><span class="sxs-lookup"><span data-stu-id="45c6c-140">n/a</span></span><br/>        | <span data-ttu-id="45c6c-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="45c6c-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="45c6c-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="45c6c-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="45c6c-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="45c6c-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="45c6c-144">string</span><span class="sxs-lookup"><span data-stu-id="45c6c-144">string</span></span><br/> | <span data-ttu-id="45c6c-145">N/D</span><span class="sxs-lookup"><span data-stu-id="45c6c-145">n/a</span></span><br/>        | <span data-ttu-id="45c6c-146">Automática, manual.</span><span class="sxs-lookup"><span data-stu-id="45c6c-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="45c6c-147">Define el modo dúplex.</span><span class="sxs-lookup"><span data-stu-id="45c6c-147">Defines the duplex mode.</span></span> <span data-ttu-id="45c6c-148">El hardware automático realiza la operación dúplex automática.</span><span class="sxs-lookup"><span data-stu-id="45c6c-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="45c6c-149">El software y el usuario realizan la función de dúplex manual.</span><span class="sxs-lookup"><span data-stu-id="45c6c-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="45c6c-150">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="45c6c-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="45c6c-151">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="45c6c-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="45c6c-152">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="45c6c-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
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

## <a name="related-topics"></a><span data-ttu-id="45c6c-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45c6c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c6c-154">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="45c6c-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




