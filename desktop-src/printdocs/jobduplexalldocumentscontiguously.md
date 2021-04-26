---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e5ae88213af15b53f71e406b4caf791b80f286f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998222"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="9d20b-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="9d20b-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="9d20b-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9d20b-105">This topic is not current.</span></span> <span data-ttu-id="9d20b-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9d20b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d20b-107">Describe las características dúplex de la salida.</span><span class="sxs-lookup"><span data-stu-id="9d20b-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="9d20b-108">La característica dúplex permite imprimir en ambos lados del medio.</span><span class="sxs-lookup"><span data-stu-id="9d20b-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="9d20b-109">Todos los documentos del trabajo se dúplex juntos de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="9d20b-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="9d20b-110">JobDuplexAllDocumentsContiguously y DocumentDuplex son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="9d20b-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="9d20b-111">Es el controlador quien determina el control de restricciones entre estas palabras clave.</span><span class="sxs-lookup"><span data-stu-id="9d20b-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="9d20b-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9d20b-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9d20b-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9d20b-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9d20b-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9d20b-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9d20b-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9d20b-115">Element Information</span></span>



| <span data-ttu-id="9d20b-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d20b-116">Name</span></span> | <span data-ttu-id="9d20b-117">Value</span><span class="sxs-lookup"><span data-stu-id="9d20b-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9d20b-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9d20b-118">Element Type</span></span> <br/>   | <span data-ttu-id="9d20b-119">Característica</span><span class="sxs-lookup"><span data-stu-id="9d20b-119">Feature</span></span><br/> |
| <span data-ttu-id="9d20b-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9d20b-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9d20b-121">Trabajo</span><span class="sxs-lookup"><span data-stu-id="9d20b-121">Job</span></span><br/>     |
| <span data-ttu-id="9d20b-122">Notas</span><span class="sxs-lookup"><span data-stu-id="9d20b-122">Notes</span></span> <br/>          | <span data-ttu-id="9d20b-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d20b-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9d20b-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9d20b-124">Structural Content</span></span>

<span data-ttu-id="9d20b-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9d20b-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9d20b-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9d20b-126">Structure Variables</span></span>

<span data-ttu-id="9d20b-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9d20b-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9d20b-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d20b-128">Name</span></span>                               | <span data-ttu-id="9d20b-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9d20b-129">Data type</span></span>         | <span data-ttu-id="9d20b-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="9d20b-130">Unit</span></span>                  | <span data-ttu-id="9d20b-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9d20b-131">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="9d20b-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="9d20b-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d20b-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9d20b-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9d20b-134">string</span><span class="sxs-lookup"><span data-stu-id="9d20b-134">string</span></span><br/> | <span data-ttu-id="9d20b-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="9d20b-135">characters</span></span><br/> | <span data-ttu-id="9d20b-136">Nombre completo válido tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="9d20b-136">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="9d20b-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9d20b-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9d20b-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9d20b-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="9d20b-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9d20b-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9d20b-140">string</span><span class="sxs-lookup"><span data-stu-id="9d20b-140">string</span></span><br/> | <span data-ttu-id="9d20b-141">N/D</span><span class="sxs-lookup"><span data-stu-id="9d20b-141">n/a</span></span><br/>        | <span data-ttu-id="9d20b-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="9d20b-142">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="9d20b-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9d20b-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="9d20b-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="9d20b-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="9d20b-145">string</span><span class="sxs-lookup"><span data-stu-id="9d20b-145">string</span></span><br/> | <span data-ttu-id="9d20b-146">N/D</span><span class="sxs-lookup"><span data-stu-id="9d20b-146">n/a</span></span><br/>        | <span data-ttu-id="9d20b-147">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="9d20b-147">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="9d20b-148">Define el modo dúplex.</span><span class="sxs-lookup"><span data-stu-id="9d20b-148">Defines the duplex mode.</span></span> <span data-ttu-id="9d20b-149">El dúplex automático lo realiza el hardware.</span><span class="sxs-lookup"><span data-stu-id="9d20b-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="9d20b-150">El dúplex manual lo realizan el software y el usuario.</span><span class="sxs-lookup"><span data-stu-id="9d20b-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9d20b-151">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9d20b-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9d20b-152">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9d20b-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9d20b-153">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9d20b-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9d20b-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d20b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d20b-155">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9d20b-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




