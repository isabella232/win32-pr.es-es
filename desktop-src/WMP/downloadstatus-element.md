---
title: Elemento DownloadStatus (msfeeds. h)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Elemento DownloadStatus Media Player Windows
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699826"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="e924e-105">Elemento DownloadStatus</span><span class="sxs-lookup"><span data-stu-id="e924e-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="e924e-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="e924e-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e924e-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e924e-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e924e-108">El elemento **DownloadStatus** especifica una dirección URL que Windows Media Player muestra como un vínculo para permitir que los usuarios vean el estado de la descarga.</span><span class="sxs-lookup"><span data-stu-id="e924e-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="e924e-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="e924e-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="e924e-110"><span id="URL"></span><span id="url"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="e924e-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="e924e-111">Dirección URL de la página web que la tienda en línea muestra para mostrar el estado de descarga al usuario.</span><span class="sxs-lookup"><span data-stu-id="e924e-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="e924e-112">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="e924e-112">Parent/Child Elements</span></span>



| <span data-ttu-id="e924e-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e924e-113">Hierarchy</span></span>       | <span data-ttu-id="e924e-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="e924e-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="e924e-115">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e924e-115">Parent elements</span></span> | <span data-ttu-id="e924e-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e924e-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="e924e-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e924e-117">Child elements</span></span>  | <span data-ttu-id="e924e-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e924e-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="e924e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e924e-119">Remarks</span></span>

<span data-ttu-id="e924e-120">Windows Media Player muestra un mensaje a los usuarios cuando hay una descarga en curso.</span><span class="sxs-lookup"><span data-stu-id="e924e-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="e924e-121">Si los servicios activos actuales definen una dirección URL de estado de descarga, el usuario puede hacer clic en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e924e-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="e924e-122">Cuando el usuario hace clic en el mensaje, el reproductor navega a la dirección URL especificada por el elemento **DownloadStatus** para que el almacén activo actual pueda proporcionar detalles sobre las descargas en curso.</span><span class="sxs-lookup"><span data-stu-id="e924e-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="e924e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e924e-123">Requirements</span></span>



| <span data-ttu-id="e924e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e924e-124">Requirement</span></span> | <span data-ttu-id="e924e-125">Value</span><span class="sxs-lookup"><span data-stu-id="e924e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e924e-126">Versión</span><span class="sxs-lookup"><span data-stu-id="e924e-126">Version</span></span><br/> | <span data-ttu-id="e924e-127">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="e924e-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="e924e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e924e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e924e-129"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="e924e-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e924e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e924e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e924e-131">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e924e-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e924e-132">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="e924e-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e924e-133">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e924e-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





