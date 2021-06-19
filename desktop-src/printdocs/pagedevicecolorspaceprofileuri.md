---
description: Obtenga información sobre el parámetro PageDeviceColorSpaceProfileURI. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396650"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="4d1b8-105">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="4d1b8-105">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="4d1b8-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-106">This topic is not current.</span></span> <span data-ttu-id="4d1b8-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4d1b8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d1b8-108">Especifica un URI relativo a la raíz del paquete a un perfil DE CEDIDO contenido en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-108">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="4d1b8-109">El procesamiento de esta opción depende de la configuración de la característica PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="4d1b8-110">Se supone que todos los elementos que usan ese perfil ya están en el espacio de color del dispositivo adecuado y no se administrarán por colores en el controlador o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="4d1b8-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d1b8-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4d1b8-112">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4d1b8-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4d1b8-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d1b8-113">Element Information</span></span>



| <span data-ttu-id="4d1b8-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d1b8-114">Name</span></span> | <span data-ttu-id="4d1b8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4d1b8-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1b8-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4d1b8-116">Element Type</span></span> <br/>   | <span data-ttu-id="4d1b8-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4d1b8-117">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4d1b8-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4d1b8-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4d1b8-119">Página</span><span class="sxs-lookup"><span data-stu-id="4d1b8-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d1b8-120">Notas</span><span class="sxs-lookup"><span data-stu-id="4d1b8-120">Notes</span></span> <br/>          | <span data-ttu-id="4d1b8-121">Esto solo se aplica a los documentos XPS y no se debe usar en PrintTickets arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-121">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="4d1b8-122">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4d1b8-123">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4d1b8-124">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4d1b8-125">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4d1b8-126">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4d1b8-127">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4d1b8-127">Structure Content</span></span>

<span data-ttu-id="4d1b8-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="4d1b8-128">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="4d1b8-129">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="4d1b8-129">Structure Properties</span></span>

<span data-ttu-id="4d1b8-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4d1b8-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4d1b8-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d1b8-131">Property</span></span>                | <span data-ttu-id="4d1b8-132">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4d1b8-132">xsi:type</span></span>           | <span data-ttu-id="4d1b8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4d1b8-133">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4d1b8-134">DataType</span><span class="sxs-lookup"><span data-stu-id="4d1b8-134">DataType</span></span><br/>     | <span data-ttu-id="4d1b8-135">string</span><span class="sxs-lookup"><span data-stu-id="4d1b8-135">string</span></span><br/>  | <span data-ttu-id="4d1b8-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="4d1b8-136">xs:string</span></span><br/>       |
| <span data-ttu-id="4d1b8-137">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4d1b8-137">DefaultValue</span></span><br/> | <span data-ttu-id="4d1b8-138">string</span><span class="sxs-lookup"><span data-stu-id="4d1b8-138">string</span></span><br/>  | <span data-ttu-id="4d1b8-139">no definido</span><span class="sxs-lookup"><span data-stu-id="4d1b8-139">undefined</span></span><br/>       |
| <span data-ttu-id="4d1b8-140">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4d1b8-140">MaxLength</span></span><br/>    | <span data-ttu-id="4d1b8-141">integer</span><span class="sxs-lookup"><span data-stu-id="4d1b8-141">integer</span></span><br/> | <span data-ttu-id="4d1b8-142">no definido</span><span class="sxs-lookup"><span data-stu-id="4d1b8-142">undefined</span></span><br/>       |
| <span data-ttu-id="4d1b8-143">MinLength</span><span class="sxs-lookup"><span data-stu-id="4d1b8-143">MinLength</span></span><br/>    | <span data-ttu-id="4d1b8-144">integer</span><span class="sxs-lookup"><span data-stu-id="4d1b8-144">integer</span></span><br/> | <span data-ttu-id="4d1b8-145">1</span><span class="sxs-lookup"><span data-stu-id="4d1b8-145">1</span></span><br/>               |
| <span data-ttu-id="4d1b8-146">Mandatory</span><span class="sxs-lookup"><span data-stu-id="4d1b8-146">Mandatory</span></span><br/>    | <span data-ttu-id="4d1b8-147">string</span><span class="sxs-lookup"><span data-stu-id="4d1b8-147">string</span></span><br/>  | <span data-ttu-id="4d1b8-148">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4d1b8-148">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4d1b8-149">UnitType</span><span class="sxs-lookup"><span data-stu-id="4d1b8-149">UnitType</span></span><br/>     | <span data-ttu-id="4d1b8-150">string</span><span class="sxs-lookup"><span data-stu-id="4d1b8-150">string</span></span><br/>  | <span data-ttu-id="4d1b8-151">caracteres</span><span class="sxs-lookup"><span data-stu-id="4d1b8-151">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4d1b8-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d1b8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d1b8-153">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4d1b8-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




