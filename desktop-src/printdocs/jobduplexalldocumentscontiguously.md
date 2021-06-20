---
description: Obtenga información sobre el elemento JobDuplexAllDocumentsContiguously, que describe las características dúplex de la salida.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a8911a4c62644bfc073a2a9c1dcfd67dad536a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408958"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="81c21-103">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="81c21-103">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="81c21-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="81c21-104">This topic is not current.</span></span> <span data-ttu-id="81c21-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="81c21-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="81c21-106">Describe las características dúplex de la salida.</span><span class="sxs-lookup"><span data-stu-id="81c21-106">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="81c21-107">La característica dúplex permite imprimir en ambos lados del medio.</span><span class="sxs-lookup"><span data-stu-id="81c21-107">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="81c21-108">Todos los documentos del trabajo se dúplex juntos de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="81c21-108">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="81c21-109">JobDuplexAllDocumentsContiguously y DocumentDuplex son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="81c21-109">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="81c21-110">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="81c21-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="81c21-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="81c21-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="81c21-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="81c21-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="81c21-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="81c21-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="81c21-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="81c21-114">Element Information</span></span>



| <span data-ttu-id="81c21-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="81c21-115">Name</span></span> | <span data-ttu-id="81c21-116">Valor</span><span class="sxs-lookup"><span data-stu-id="81c21-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="81c21-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="81c21-117">Element Type</span></span> <br/>   | <span data-ttu-id="81c21-118">Característica</span><span class="sxs-lookup"><span data-stu-id="81c21-118">Feature</span></span><br/> |
| <span data-ttu-id="81c21-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="81c21-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="81c21-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="81c21-120">Job</span></span><br/>     |
| <span data-ttu-id="81c21-121">Notas</span><span class="sxs-lookup"><span data-stu-id="81c21-121">Notes</span></span> <br/>          | <span data-ttu-id="81c21-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="81c21-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="81c21-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="81c21-123">Structural Content</span></span>

<span data-ttu-id="81c21-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="81c21-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="81c21-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="81c21-125">Structure Variables</span></span>

<span data-ttu-id="81c21-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="81c21-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="81c21-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="81c21-127">Name</span></span>                               | <span data-ttu-id="81c21-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="81c21-128">Data type</span></span>         | <span data-ttu-id="81c21-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="81c21-129">Unit</span></span>                  | <span data-ttu-id="81c21-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="81c21-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="81c21-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="81c21-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81c21-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="81c21-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="81c21-133">string</span><span class="sxs-lookup"><span data-stu-id="81c21-133">string</span></span><br/> | <span data-ttu-id="81c21-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="81c21-134">characters</span></span><br/> | <span data-ttu-id="81c21-135">Nombre completo válido tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="81c21-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="81c21-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81c21-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="81c21-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="81c21-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="81c21-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="81c21-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="81c21-139">string</span><span class="sxs-lookup"><span data-stu-id="81c21-139">string</span></span><br/> | <span data-ttu-id="81c21-140">N/D</span><span class="sxs-lookup"><span data-stu-id="81c21-140">n/a</span></span><br/>        | <span data-ttu-id="81c21-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="81c21-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="81c21-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="81c21-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="81c21-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="81c21-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="81c21-144">string</span><span class="sxs-lookup"><span data-stu-id="81c21-144">string</span></span><br/> | <span data-ttu-id="81c21-145">N/D</span><span class="sxs-lookup"><span data-stu-id="81c21-145">n/a</span></span><br/>        | <span data-ttu-id="81c21-146">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="81c21-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="81c21-147">Define el modo dúplex.</span><span class="sxs-lookup"><span data-stu-id="81c21-147">Defines the duplex mode.</span></span> <span data-ttu-id="81c21-148">El dúplex automático lo realiza el hardware.</span><span class="sxs-lookup"><span data-stu-id="81c21-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="81c21-149">El dúplex manual lo realizan el software y el usuario.</span><span class="sxs-lookup"><span data-stu-id="81c21-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="81c21-150">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="81c21-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="81c21-151">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="81c21-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="81c21-152">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="81c21-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="81c21-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81c21-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c21-154">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="81c21-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




