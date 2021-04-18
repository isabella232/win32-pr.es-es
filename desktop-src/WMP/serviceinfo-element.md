---
title: ServiceInfo, elemento
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento ServiceInfo es el elemento principal del documento ServiceInfo.xml.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Elemento ServiceInfo Media Player Windows
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649822"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="42f5e-106">ServiceInfo, elemento</span><span class="sxs-lookup"><span data-stu-id="42f5e-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="42f5e-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="42f5e-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="42f5e-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="42f5e-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="42f5e-109">El elemento **ServiceInfo** es el elemento principal del documento ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="42f5e-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="42f5e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="42f5e-110">Attributes</span></span>



| <span data-ttu-id="42f5e-111">Término</span><span class="sxs-lookup"><span data-stu-id="42f5e-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="42f5e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="42f5e-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f5e-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versión** (opcional)</span><span class="sxs-lookup"><span data-stu-id="42f5e-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="42f5e-114">Versión del archivo de ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="42f5e-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="42f5e-115">La versión 1,00 es compatible con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="42f5e-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="42f5e-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Clave** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="42f5e-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="42f5e-117">Cadena de clave de servicio que identifica de forma única la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="42f5e-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="42f5e-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span><span class="sxs-lookup"><span data-stu-id="42f5e-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="42f5e-119">Indica si la tienda en línea es un almacén de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="42f5e-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="42f5e-120">Un valor de "true" indica que el almacén es un almacén de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="42f5e-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="42f5e-121">Un valor de "false" indica que el almacén no es un almacén de tipo 1; es decir, es un almacén de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="42f5e-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="42f5e-122">El valor predeterminado es "false".</span><span class="sxs-lookup"><span data-stu-id="42f5e-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="42f5e-123">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="42f5e-123">Parent/Child Elements</span></span>



| <span data-ttu-id="42f5e-124">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="42f5e-124">Hierarchy</span></span>       | <span data-ttu-id="42f5e-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="42f5e-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f5e-126">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="42f5e-126">Parent elements</span></span> | <span data-ttu-id="42f5e-127">None</span><span class="sxs-lookup"><span data-stu-id="42f5e-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="42f5e-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="42f5e-128">Child elements</span></span>  | <span data-ttu-id="42f5e-129">**AlbumInfo**, **BuyCD**, **color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **Infocenter**, **install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="42f5e-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="42f5e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42f5e-130">Remarks</span></span>

<span data-ttu-id="42f5e-131">En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL.</span><span class="sxs-lookup"><span data-stu-id="42f5e-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="42f5e-132">Otros pueden estar presentes para fines de compatibilidad heredada.</span><span class="sxs-lookup"><span data-stu-id="42f5e-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="42f5e-133">La solicitud también incluirá los parámetros especificados mediante el parámetro de línea de comandos ServiceExtra de Windows Media Player el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="42f5e-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="42f5e-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="42f5e-134">Name</span></span>         | <span data-ttu-id="42f5e-135">Value</span><span class="sxs-lookup"><span data-stu-id="42f5e-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f5e-136">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="42f5e-136">*geoid*</span></span>      | <span data-ttu-id="42f5e-137">IDENTIFICADOR de ubicación geográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="42f5e-137">Windows geographical location ID.</span></span> <span data-ttu-id="42f5e-138">El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="42f5e-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="42f5e-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="42f5e-139">*locale*</span></span>     | <span data-ttu-id="42f5e-140">IDENTIFICADOR de configuración regional de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="42f5e-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="42f5e-141">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="42f5e-141">*userlocale*</span></span> | <span data-ttu-id="42f5e-142">IDENTIFICADOR de configuración regional de Windows.</span><span class="sxs-lookup"><span data-stu-id="42f5e-142">Windows locale ID.</span></span> <span data-ttu-id="42f5e-143">El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="42f5e-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="42f5e-144">*version*</span><span class="sxs-lookup"><span data-stu-id="42f5e-144">*version*</span></span>    | <span data-ttu-id="42f5e-145">Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="42f5e-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="42f5e-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f5e-146">Requirements</span></span>



| <span data-ttu-id="42f5e-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f5e-147">Requirement</span></span> | <span data-ttu-id="42f5e-148">Value</span><span class="sxs-lookup"><span data-stu-id="42f5e-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="42f5e-149">Versión</span><span class="sxs-lookup"><span data-stu-id="42f5e-149">Version</span></span><br/> | <span data-ttu-id="42f5e-150">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42f5e-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42f5e-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f5e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f5e-152">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="42f5e-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="42f5e-153">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="42f5e-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="42f5e-154">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="42f5e-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





