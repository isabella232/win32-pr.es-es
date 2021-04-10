---
description: Las aplicaciones, incluidos los servicios, pueden registrarse para recibir notificaciones de eventos de dispositivo.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Eventos de dispositivo (IoEvent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274825"
---
# <a name="device-events-ioeventh"></a><span data-ttu-id="d33af-103">Eventos de dispositivo (IoEvent. h)</span><span class="sxs-lookup"><span data-stu-id="d33af-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="d33af-104">Las aplicaciones, incluidos los servicios, pueden registrarse para recibir notificaciones de eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d33af-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="d33af-105">Por ejemplo, un servicio de catálogo puede recibir un aviso de los volúmenes que se montan o desmontan, por lo que puede ajustar las rutas de acceso a los archivos del volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="d33af-106">El sistema notifica a una aplicación que se ha producido un evento de dispositivo mediante el envío de un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d33af-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="d33af-107">El sistema notifica a un servicio que se ha producido un evento de dispositivo mediante la invocación de la función de controlador de eventos del servicio, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="d33af-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="d33af-108">Para recibir avisos de eventos de dispositivo, llame a la función [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) con una estructura de [**controlador de \_ difusión \_ de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="d33af-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="d33af-109">Asegúrese de establecer el miembro **de \_ identificador de dbch** en el identificador de dispositivo Obtenido de la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="d33af-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="d33af-110">Además, establezca el miembro de **dbch \_ DeviceType** en **DBT \_ DEVTYP \_ Handle**.</span><span class="sxs-lookup"><span data-stu-id="d33af-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="d33af-111">La función devuelve un identificador de notificación de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d33af-111">The function returns a device notification handle.</span></span> <span data-ttu-id="d33af-112">Tenga en cuenta que esto no es lo mismo que el identificador de volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="d33af-113">Cuando la aplicación recibe una notificación, si el tipo de evento es [DBT \_ CUSTOMEVENT](dbt-customevent.md), es posible que haya recibido uno de los eventos de dispositivo definidos en IoEvent. h.</span><span class="sxs-lookup"><span data-stu-id="d33af-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="d33af-114">Para determinar si se ha producido uno de estos eventos, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d33af-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="d33af-115">Trate los datos de evento como una estructura [**\_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="d33af-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="d33af-116">Compruebe que el miembro de **dbch \_ DeviceType** está establecido en **DBT \_ DEVTYP \_ Handle**.</span><span class="sxs-lookup"><span data-stu-id="d33af-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="d33af-117">Si **dbch \_ DeviceType** es **DBT \_ DEVTYP \_ Handle**, los datos de evento son, en realidad, un puntero a una estructura de [**\_ \_ controlador de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="d33af-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="d33af-118">Compare el **miembro \_ eventguid de dbch** con los **GUID** que aparecen en la siguiente tabla mediante la función [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .</span><span class="sxs-lookup"><span data-stu-id="d33af-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="d33af-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**\_ \_ bloqueo exclusivo de CDROM de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="d33af-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="d33af-121">El dispositivo de CD-ROM se ha bloqueado para acceso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d33af-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="d33af-122">**Windows Server 2003 y Windows XP:** La compatibilidad con este valor requiere IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="d33af-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="d33af-123">Para obtener más información, consulte [Image Mastering API](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="d33af-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**\_ \_ \_ desbloqueo exclusivo de CDROM de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="d33af-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="d33af-126">Se ha desbloqueado un dispositivo de CD-ROM que estaba bloqueado para acceso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d33af-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="d33af-127">**Windows Server 2003 y Windows XP:** La compatibilidad con este valor requiere IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="d33af-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="d33af-128">Para obtener más información, consulte [Image Mastering API](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="d33af-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**el \_ dispositivo de e/s de GUID \_ \_ \_ está listo**</span><span class="sxs-lookup"><span data-stu-id="d33af-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="d33af-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="d33af-131">El proceso de ejecución multimedia está en curso.</span><span class="sxs-lookup"><span data-stu-id="d33af-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ solicitud externa de dispositivo de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="d33af-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="d33af-134">Hay varias causas posibles para este evento: para obtener más información, consulte especificación de la especificación de MMC de T10 del comando GET EVENT STATUs NOTIFICATION, en [https://www.t10.org/](https://www.t10.org/) .</span><span class="sxs-lookup"><span data-stu-id="d33af-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_llegada de medios de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="d33af-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="d33af-137">Se han agregado medios extraíbles al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d33af-137">Removable media has been added to the device.</span></span> <span data-ttu-id="d33af-138">El miembro de **\_ datos dbch** es un puntero a una estructura de [**contexto de cambio de medios de clase \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="d33af-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="d33af-139">El miembro **NewState** proporciona información de estado.</span><span class="sxs-lookup"><span data-stu-id="d33af-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="d33af-140">Por ejemplo, un valor de **MediaUnavailable** indica que el medio no está disponible (por ejemplo, debido a una sesión de grabación activa).</span><span class="sxs-lookup"><span data-stu-id="d33af-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="d33af-141">**Windows XP:** El miembro de **\_ datos dbch** es un valor **ULong** que representa el número de veces que se ha cambiado el contenido multimedia desde el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d33af-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_solicitud de \_ \_ expulsión de medios de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="d33af-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="d33af-144">La unidad del medio extraíble ha recibido una solicitud del usuario para expulsar la ranura o el medio especificado.</span><span class="sxs-lookup"><span data-stu-id="d33af-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_eliminación de medios de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="d33af-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="d33af-147">Los medios extraíbles se han quitado del dispositivo o no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="d33af-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="d33af-148">El miembro de **\_ datos dbch** es un puntero a una estructura de [**contexto de cambio de medios de clase \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="d33af-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="d33af-149">El miembro **NewState** proporciona información de estado.</span><span class="sxs-lookup"><span data-stu-id="d33af-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="d33af-150">Por ejemplo, un valor de **MediaUnavailable** indica que el medio no está disponible (por ejemplo, debido a una sesión de grabación activa).</span><span class="sxs-lookup"><span data-stu-id="d33af-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="d33af-151">**Windows XP:** El miembro de **\_ datos dbch** es un valor **ULong** que representa el número de veces que se ha cambiado el contenido multimedia desde el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d33af-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_cambio de volumen de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-153">7373654a-812a-11d0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="d33af-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="d33af-154">La etiqueta del volumen ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d33af-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_tamaño de \_ cambio de volumen de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span><span class="sxs-lookup"><span data-stu-id="d33af-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="d33af-157">El tamaño del sistema de archivos del volumen ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d33af-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="d33af-158">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="d33af-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**Desmontaje del \_ volumen de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="d33af-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="d33af-161">Está en curso un intento de desmontar el volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="d33af-162">Debe cerrar todos los identificadores de los archivos y directorios del volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="d33af-163">Este evento no estará necesariamente precedido por un evento **de \_ \_ \_ bloqueo de volumen de e/s de GUID** .</span><span class="sxs-lookup"><span data-stu-id="d33af-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ \_ no se pudo desmontar el volumen de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="d33af-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="d33af-166">Error al tratar de desmontar un volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="d33af-167">Esto suele ocurrir porque otro proceso no pudo responder a un aviso de **\_ \_ \_ desmontaje de volumen de e/s de GUID** cerrando los identificadores pendientes.</span><span class="sxs-lookup"><span data-stu-id="d33af-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="d33af-168">Dado que se produjo un error al desmontar, puede volver a abrir los identificadores del volumen afectado.</span><span class="sxs-lookup"><span data-stu-id="d33af-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_cambio de \_ Estado de FVE de volumen de e/s de \_ \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="d33af-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="d33af-171">El estado de Cifrado de unidad BitLocker del volumen ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d33af-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="d33af-172">Este evento se señala cuando BitLocker está habilitado o deshabilitado, o cuando se inicia, finaliza, pausa o reanuda el cifrado.</span><span class="sxs-lookup"><span data-stu-id="d33af-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="d33af-173">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="d33af-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_bloqueo de volumen de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-175">50708874-c9af-11D1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="d33af-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="d33af-176">Otro proceso está intentando bloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="d33af-177">Debe cerrar todos los identificadores de los archivos y directorios del volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_error de \_ bloqueo de volumen de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="d33af-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="d33af-180">Error al tratar de bloquear un volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="d33af-181">Esto suele ocurrir porque otro proceso no pudo responder a un evento de **\_ bloqueo de \_ volumen \_ de e/s de GUID** cerrando los identificadores pendientes.</span><span class="sxs-lookup"><span data-stu-id="d33af-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="d33af-182">Debido a que se produjo un error en el bloqueo, puede volver a abrir los identificadores del volumen afectado.</span><span class="sxs-lookup"><span data-stu-id="d33af-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montaje de volumen de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="d33af-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="d33af-185">Otro proceso ha montado el volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="d33af-186">Puede abrir uno o más identificadores en él.</span><span class="sxs-lookup"><span data-stu-id="d33af-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_cambio de \_ nombre de volumen de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-188">2de97f83-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="d33af-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="d33af-189">Se ha cambiado el nombre del volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**el \_ volumen de e/s de GUID \_ \_ necesita \_ CHKDSK**</span><span class="sxs-lookup"><span data-stu-id="d33af-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="d33af-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="d33af-192">Un sistema de archivos ha detectado daños en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="d33af-193">La aplicación debe ejecutar CHKDSK en el volumen o notificar al usuario que lo haga.</span><span class="sxs-lookup"><span data-stu-id="d33af-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="d33af-194">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="d33af-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_cambio de \_ \_ configuración física \_ de volumen de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-196">2de97f84-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="d33af-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="d33af-197">Ha cambiado la estructura física o el estado físico actual del volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**\_volumen de e/s de GUID \_ preparación de \_ \_ expulsión**</span><span class="sxs-lookup"><span data-stu-id="d33af-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="d33af-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="d33af-200">El sistema de archivos está preparando el disco que se va a expulsar.</span><span class="sxs-lookup"><span data-stu-id="d33af-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="d33af-201">Por ejemplo, el sistema de archivos está deteniendo una operación de formato en segundo plano o cerrando la sesión en un medio de escritura.</span><span class="sxs-lookup"><span data-stu-id="d33af-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="d33af-202">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="d33af-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_cambio de \_ \_ identificador único \_ de volumen de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="d33af-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="d33af-205">Se ha cambiado el identificador único del volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="d33af-206">Para obtener más información sobre el identificador único, consulte [**ioctl \_ MOUNTDEV \_ query \_ Unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span><span class="sxs-lookup"><span data-stu-id="d33af-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="d33af-207">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite hasta Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d33af-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**desbloqueo del volumen de \_ e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="d33af-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="d33af-210">Otro proceso ha desbloqueado el volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="d33af-211">Puede abrir uno o más identificadores en él.</span><span class="sxs-lookup"><span data-stu-id="d33af-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d33af-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**\_volumen de e/s de GUID \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33af-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="d33af-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="d33af-214">El contenido multimedia se está agotando. Este evento se envía cuando un sistema de archivos determina que la tasa de errores de un volumen es demasiado alta o que el espacio de sustitución del defecto está casi agotado.</span><span class="sxs-lookup"><span data-stu-id="d33af-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="d33af-215">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="d33af-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d33af-216">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d33af-216">Remarks</span></span>

<span data-ttu-id="d33af-217">Los eventos de **\_ \_ \_ \_ error** de desmontaje de volumen de e/s de GUID e e/s de GUID están relacionados, al igual que los eventos de **\_ \_ \_** error de bloqueo de volumen de e/s de GUID e e **\_ /s \_ \_ \_** . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="d33af-218">Los eventos de bloqueo de volumen de e/s de GUID e e **\_ /s \_ \_** de GUID indican que se está intentando realizar una operación. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d33af-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="d33af-219">Debe actuar en la notificación de eventos y registrar la acción realizada.</span><span class="sxs-lookup"><span data-stu-id="d33af-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="d33af-220">Error **de \_ \_ \_ desmontaje \_ de volumen de e** /s de GUID y eventos de **\_ \_ \_ \_ error de bloqueo de volumen de e/s de GUID** indican que se produjo un error en la operación</span><span class="sxs-lookup"><span data-stu-id="d33af-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="d33af-221">Después, puede usar el registro para deshacer las acciones realizadas en respuesta a la operación.</span><span class="sxs-lookup"><span data-stu-id="d33af-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="d33af-222">El miembro **dbch \_ hdevnotify** de la estructura de [**\_ \_ control de difusión de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica el dispositivo afectado.</span><span class="sxs-lookup"><span data-stu-id="d33af-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="d33af-223">Tenga en cuenta que se trata del identificador de notificación de dispositivo devuelto por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), no por un identificador de volumen.</span><span class="sxs-lookup"><span data-stu-id="d33af-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="d33af-224">Para realizar operaciones en el volumen, asigne este identificador al identificador de volumen correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d33af-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="d33af-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d33af-225">Requirements</span></span>



| <span data-ttu-id="d33af-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="d33af-226">Requirement</span></span> | <span data-ttu-id="d33af-227">Value</span><span class="sxs-lookup"><span data-stu-id="d33af-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d33af-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d33af-228">Minimum supported client</span></span><br/> | <span data-ttu-id="d33af-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d33af-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="d33af-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d33af-230">Minimum supported server</span></span><br/> | <span data-ttu-id="d33af-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d33af-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="d33af-232">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d33af-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="d33af-233"><dt>IoEvent. h</dt></span><span class="sxs-lookup"><span data-stu-id="d33af-233"><dt>IoEvent.h</dt></span></span> </dl> |



 

