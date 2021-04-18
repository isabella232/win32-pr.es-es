---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4536251150851ad02abf41ca26ffaa36699281db
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707616"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="63e63-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="63e63-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="63e63-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="63e63-105">This topic is not current.</span></span> <span data-ttu-id="63e63-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63e63-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63e63-107">Especifica un URI relativo a la raíz del paquete para un perfil de ICC incluido en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="63e63-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="63e63-108">El procesamiento de esta opción depende del valor de la característica PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="63e63-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="63e63-109">Se supone que todos los elementos que usan ese perfil ya están en el espacio de colores del dispositivo adecuado y no se administrarán en color en el controlador o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63e63-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="63e63-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="63e63-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63e63-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="63e63-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="63e63-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="63e63-112">Element Information</span></span>



| <span data-ttu-id="63e63-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="63e63-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e63-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="63e63-114">Element Type</span></span> <br/>   | <span data-ttu-id="63e63-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="63e63-115">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="63e63-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="63e63-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63e63-117">Página</span><span class="sxs-lookup"><span data-stu-id="63e63-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="63e63-118">Notas</span><span class="sxs-lookup"><span data-stu-id="63e63-118">Notes</span></span> <br/>          | <span data-ttu-id="63e63-119">Esto se aplica a los documentos XPS únicamente y no se debe usar en elementos PrintTicket arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="63e63-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="63e63-120">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="63e63-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="63e63-121">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="63e63-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="63e63-122">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="63e63-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="63e63-123">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="63e63-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="63e63-124">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63e63-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="63e63-125">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="63e63-125">Structure Content</span></span>

<span data-ttu-id="63e63-126">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="63e63-126">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="63e63-127">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="63e63-127">Structure Properties</span></span>

<span data-ttu-id="63e63-128">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="63e63-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63e63-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63e63-129">Property</span></span>                | <span data-ttu-id="63e63-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="63e63-130">xsi:type</span></span>           | <span data-ttu-id="63e63-131">Value</span><span class="sxs-lookup"><span data-stu-id="63e63-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="63e63-132">DataType</span><span class="sxs-lookup"><span data-stu-id="63e63-132">DataType</span></span><br/>     | <span data-ttu-id="63e63-133">string</span><span class="sxs-lookup"><span data-stu-id="63e63-133">string</span></span><br/>  | <span data-ttu-id="63e63-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="63e63-134">xs:string</span></span><br/>       |
| <span data-ttu-id="63e63-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="63e63-135">DefaultValue</span></span><br/> | <span data-ttu-id="63e63-136">string</span><span class="sxs-lookup"><span data-stu-id="63e63-136">string</span></span><br/>  | <span data-ttu-id="63e63-137">no definido</span><span class="sxs-lookup"><span data-stu-id="63e63-137">undefined</span></span><br/>       |
| <span data-ttu-id="63e63-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="63e63-138">MaxLength</span></span><br/>    | <span data-ttu-id="63e63-139">integer</span><span class="sxs-lookup"><span data-stu-id="63e63-139">integer</span></span><br/> | <span data-ttu-id="63e63-140">no definido</span><span class="sxs-lookup"><span data-stu-id="63e63-140">undefined</span></span><br/>       |
| <span data-ttu-id="63e63-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="63e63-141">MinLength</span></span><br/>    | <span data-ttu-id="63e63-142">integer</span><span class="sxs-lookup"><span data-stu-id="63e63-142">integer</span></span><br/> | <span data-ttu-id="63e63-143">1</span><span class="sxs-lookup"><span data-stu-id="63e63-143">1</span></span><br/>               |
| <span data-ttu-id="63e63-144">Mandatory</span><span class="sxs-lookup"><span data-stu-id="63e63-144">Mandatory</span></span><br/>    | <span data-ttu-id="63e63-145">string</span><span class="sxs-lookup"><span data-stu-id="63e63-145">string</span></span><br/>  | <span data-ttu-id="63e63-146">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="63e63-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="63e63-147">UnitType</span><span class="sxs-lookup"><span data-stu-id="63e63-147">UnitType</span></span><br/>     | <span data-ttu-id="63e63-148">string</span><span class="sxs-lookup"><span data-stu-id="63e63-148">string</span></span><br/>  | <span data-ttu-id="63e63-149">caracteres</span><span class="sxs-lookup"><span data-stu-id="63e63-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="63e63-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63e63-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63e63-151">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="63e63-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




