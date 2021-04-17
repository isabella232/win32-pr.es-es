---
description: Enviado por el filtro de lector ASF de WM cuando lee archivos ASF protegidos por la administración de derechos digitales (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653393"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="f3c00-103">EC_WMT_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="f3c00-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="f3c00-104">Enviado por el filtro de [lector ASF de WM](wm-asf-reader-filter.md) cuando lee archivos ASF protegidos por la administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="f3c00-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="f3c00-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3c00-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3c00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f3c00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f3c00-107">Uno de los siguientes valores de **\_ Estado de WMT** :</span><span class="sxs-lookup"><span data-stu-id="f3c00-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="f3c00-108">Value</span><span class="sxs-lookup"><span data-stu-id="f3c00-108">Value</span></span>                         | <span data-ttu-id="f3c00-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3c00-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c00-110">\_licencia de adquisición de WMT \_</span><span class="sxs-lookup"><span data-stu-id="f3c00-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="f3c00-111">Se envía cuando el componente DRM ha completado el proceso de adquisición de licencias, ya sea correcta o incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="f3c00-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="f3c00-112">individual de WMT \_</span><span class="sxs-lookup"><span data-stu-id="f3c00-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="f3c00-113">Se ha completado el proceso de actualización de seguridad, ya sea correctamente o sin éxito.</span><span class="sxs-lookup"><span data-stu-id="f3c00-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="f3c00-114">WMT \_ necesita la \_ individualización</span><span class="sxs-lookup"><span data-stu-id="f3c00-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="f3c00-115">El archivo requiere que una aplicación reciba una actualización de seguridad antes de realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="f3c00-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="f3c00-116">\_sin \_ derechos de WMT</span><span class="sxs-lookup"><span data-stu-id="f3c00-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="f3c00-117">La aplicación no tiene derechos para realizar la acción solicitada en un archivo protegido por la versión 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="f3c00-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="f3c00-118">\_no hay \_ derechos de WMT \_ ex</span><span class="sxs-lookup"><span data-stu-id="f3c00-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="f3c00-119">La aplicación no tiene derechos para realizar la acción solicitada en un archivo protegido por la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="f3c00-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="f3c00-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f3c00-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f3c00-121">Puntero a una estructura de [**\_ \_ \_ datos de evento WMT de AM**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que contiene información sobre el evento o **null**.</span><span class="sxs-lookup"><span data-stu-id="f3c00-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="f3c00-122">El miembro **pdata** de esta estructura apunta a datos adicionales, cuyo tipo depende del valor de **lParam1**, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f3c00-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="f3c00-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="f3c00-123">lParam1</span></span>                       | <span data-ttu-id="f3c00-124">\_Datos de evento WMT de AM \_ \_ . pdata</span><span class="sxs-lookup"><span data-stu-id="f3c00-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c00-125">\_licencia de adquisición de WMT \_</span><span class="sxs-lookup"><span data-stu-id="f3c00-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="f3c00-126">Puntero a una estructura de [**datos de licencia de Get de WM \_ \_ \_**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="f3c00-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="f3c00-127">Esta estructura se documenta en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="f3c00-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="f3c00-128">individual de WMT \_</span><span class="sxs-lookup"><span data-stu-id="f3c00-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="f3c00-129">Puntero a una estructura de estado de la [**\_ \_ individualización de WM**](/windows/desktop/wmformat/wm-individualize-status) .</span><span class="sxs-lookup"><span data-stu-id="f3c00-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="f3c00-130">WMT \_ necesita la \_ individualización</span><span class="sxs-lookup"><span data-stu-id="f3c00-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="f3c00-131">**Null**.</span><span class="sxs-lookup"><span data-stu-id="f3c00-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="f3c00-132">\_sin \_ derechos de WMT</span><span class="sxs-lookup"><span data-stu-id="f3c00-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="f3c00-133">Puntero a una cadena de caracteres anchos que contiene una dirección URL de desafío.</span><span class="sxs-lookup"><span data-stu-id="f3c00-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="f3c00-134">\_no hay \_ derechos de WMT \_ ex</span><span class="sxs-lookup"><span data-stu-id="f3c00-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="f3c00-135">Puntero a una estructura de [**datos de licencia de Get de WM \_ \_ \_**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="f3c00-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="f3c00-136">El valor de *lParam2* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3c00-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="f3c00-137">Compruebe el valor antes de desreferenciar el puntero.</span><span class="sxs-lookup"><span data-stu-id="f3c00-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3c00-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3c00-138">Remarks</span></span>

<span data-ttu-id="f3c00-139">Consulte la documentación del SDK de Windows Media Format para obtener más información sobre cómo habilitar la reproducción de archivos protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="f3c00-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c00-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3c00-140">Requirements</span></span>



| <span data-ttu-id="f3c00-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3c00-141">Requirement</span></span> | <span data-ttu-id="f3c00-142">Value</span><span class="sxs-lookup"><span data-stu-id="f3c00-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c00-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3c00-143">Header</span></span><br/> | <dl> <span data-ttu-id="f3c00-144"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c00-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c00-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3c00-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c00-146">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="f3c00-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f3c00-147">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3c00-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

