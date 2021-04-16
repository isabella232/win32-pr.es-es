---
title: Elemento InfoCenter
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento InfoCenter
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Elemento de InfoCenter Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699326"
---
# <a name="infocenter-element"></a><span data-ttu-id="45875-105">Elemento InfoCenter</span><span class="sxs-lookup"><span data-stu-id="45875-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="45875-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="45875-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="45875-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="45875-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="45875-108">El elemento **Infocenter** especifica la dirección URL de la página web que Windows Media Player muestra en la característica de vista de centro de información de que **ahora se reproduce** cuando la tienda en línea está activa.</span><span class="sxs-lookup"><span data-stu-id="45875-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="45875-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="45875-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="45875-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="45875-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="45875-111">Dirección URL de la página web que Windows Media Player muestra.</span><span class="sxs-lookup"><span data-stu-id="45875-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="45875-112">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="45875-112">Parent/Child Elements</span></span>



| <span data-ttu-id="45875-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="45875-113">Hierarchy</span></span>       | <span data-ttu-id="45875-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="45875-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="45875-115">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="45875-115">Parent elements</span></span> | <span data-ttu-id="45875-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="45875-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="45875-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45875-117">Child elements</span></span>  | <span data-ttu-id="45875-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="45875-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="45875-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45875-119">Remarks</span></span>

<span data-ttu-id="45875-120">El usuario controla cuándo está activa la vista centro de información.</span><span class="sxs-lookup"><span data-stu-id="45875-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="45875-121">Para recuperar información sobre el elemento multimedia que se está reproduciendo actualmente, debe incrustar una instancia de Windows Media Player control en la página web y utilizar el modelo de objetos del reproductor.</span><span class="sxs-lookup"><span data-stu-id="45875-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="45875-122">En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL.</span><span class="sxs-lookup"><span data-stu-id="45875-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="45875-123">Otros pueden estar presentes para fines de compatibilidad heredada.</span><span class="sxs-lookup"><span data-stu-id="45875-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="45875-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="45875-124">Name</span></span>         | <span data-ttu-id="45875-125">Value</span><span class="sxs-lookup"><span data-stu-id="45875-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45875-126">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="45875-126">*geoid*</span></span>      | <span data-ttu-id="45875-127">IDENTIFICADOR de ubicación geográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="45875-127">Windows geographical location ID.</span></span> <span data-ttu-id="45875-128">El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="45875-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="45875-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="45875-129">*locale*</span></span>     | <span data-ttu-id="45875-130">IDENTIFICADOR de configuración regional de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="45875-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="45875-131">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="45875-131">*userlocale*</span></span> | <span data-ttu-id="45875-132">IDENTIFICADOR de configuración regional de Windows.</span><span class="sxs-lookup"><span data-stu-id="45875-132">Windows locale ID.</span></span> <span data-ttu-id="45875-133">El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="45875-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="45875-134">*version*</span><span class="sxs-lookup"><span data-stu-id="45875-134">*version*</span></span>    | <span data-ttu-id="45875-135">Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="45875-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="45875-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45875-136">Requirements</span></span>



| <span data-ttu-id="45875-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="45875-137">Requirement</span></span> | <span data-ttu-id="45875-138">Value</span><span class="sxs-lookup"><span data-stu-id="45875-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="45875-139">Versión</span><span class="sxs-lookup"><span data-stu-id="45875-139">Version</span></span><br/> | <span data-ttu-id="45875-140">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="45875-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45875-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="45875-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45875-142">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="45875-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="45875-143">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="45875-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="45875-144">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="45875-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





