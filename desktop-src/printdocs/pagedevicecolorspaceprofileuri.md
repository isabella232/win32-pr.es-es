---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a1b4cf607ddf880311659e562647ba583a2951
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995682"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="87906-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="87906-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="87906-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="87906-105">This topic is not current.</span></span> <span data-ttu-id="87906-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87906-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87906-107">Especifica un IDENTIFICADOR URI relativo a la raíz del paquete en un perfil DE CEDIDO contenido en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="87906-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="87906-108">El procesamiento de esta opción depende de la configuración de la característica PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="87906-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="87906-109">Se supone que todos los elementos que usan ese perfil ya están en el espacio de color del dispositivo adecuado y no se administrarán por colores en el controlador o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87906-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="87906-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="87906-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87906-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="87906-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="87906-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="87906-112">Element Information</span></span>



| <span data-ttu-id="87906-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="87906-113">Name</span></span> | <span data-ttu-id="87906-114">Value</span><span class="sxs-lookup"><span data-stu-id="87906-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87906-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="87906-115">Element Type</span></span> <br/>   | <span data-ttu-id="87906-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="87906-116">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="87906-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="87906-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87906-118">Página</span><span class="sxs-lookup"><span data-stu-id="87906-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="87906-119">Notas</span><span class="sxs-lookup"><span data-stu-id="87906-119">Notes</span></span> <br/>          | <span data-ttu-id="87906-120">Esto solo se aplica a los documentos XPS y no se debe usar en PrintTickets arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="87906-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="87906-121">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso como una imagen o un perfil de color en un documento de capacidades de impresión o PrintTicket DEBE hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="87906-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="87906-122">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="87906-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="87906-123">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="87906-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="87906-124">Los URI a los que se hace referencia en un documento de capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="87906-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="87906-125">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y puedan crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="87906-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="87906-126">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="87906-126">Structure Content</span></span>

<span data-ttu-id="87906-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="87906-127">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="87906-128">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="87906-128">Structure Properties</span></span>

<span data-ttu-id="87906-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="87906-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87906-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87906-130">Property</span></span>                | <span data-ttu-id="87906-131">xsi:type</span><span class="sxs-lookup"><span data-stu-id="87906-131">xsi:type</span></span>           | <span data-ttu-id="87906-132">Value</span><span class="sxs-lookup"><span data-stu-id="87906-132">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="87906-133">DataType</span><span class="sxs-lookup"><span data-stu-id="87906-133">DataType</span></span><br/>     | <span data-ttu-id="87906-134">string</span><span class="sxs-lookup"><span data-stu-id="87906-134">string</span></span><br/>  | <span data-ttu-id="87906-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="87906-135">xs:string</span></span><br/>       |
| <span data-ttu-id="87906-136">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="87906-136">DefaultValue</span></span><br/> | <span data-ttu-id="87906-137">string</span><span class="sxs-lookup"><span data-stu-id="87906-137">string</span></span><br/>  | <span data-ttu-id="87906-138">no definido</span><span class="sxs-lookup"><span data-stu-id="87906-138">undefined</span></span><br/>       |
| <span data-ttu-id="87906-139">MaxLength</span><span class="sxs-lookup"><span data-stu-id="87906-139">MaxLength</span></span><br/>    | <span data-ttu-id="87906-140">integer</span><span class="sxs-lookup"><span data-stu-id="87906-140">integer</span></span><br/> | <span data-ttu-id="87906-141">no definido</span><span class="sxs-lookup"><span data-stu-id="87906-141">undefined</span></span><br/>       |
| <span data-ttu-id="87906-142">MinLength</span><span class="sxs-lookup"><span data-stu-id="87906-142">MinLength</span></span><br/>    | <span data-ttu-id="87906-143">integer</span><span class="sxs-lookup"><span data-stu-id="87906-143">integer</span></span><br/> | <span data-ttu-id="87906-144">1</span><span class="sxs-lookup"><span data-stu-id="87906-144">1</span></span><br/>               |
| <span data-ttu-id="87906-145">Mandatory</span><span class="sxs-lookup"><span data-stu-id="87906-145">Mandatory</span></span><br/>    | <span data-ttu-id="87906-146">string</span><span class="sxs-lookup"><span data-stu-id="87906-146">string</span></span><br/>  | <span data-ttu-id="87906-147">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="87906-147">psk:Conditional</span></span><br/> |
| <span data-ttu-id="87906-148">UnitType</span><span class="sxs-lookup"><span data-stu-id="87906-148">UnitType</span></span><br/>     | <span data-ttu-id="87906-149">string</span><span class="sxs-lookup"><span data-stu-id="87906-149">string</span></span><br/>  | <span data-ttu-id="87906-150">caracteres</span><span class="sxs-lookup"><span data-stu-id="87906-150">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="87906-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87906-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87906-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="87906-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




