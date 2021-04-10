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
# <a name="device-events-ioeventh"></a>Eventos de dispositivo (IoEvent. h)

Las aplicaciones, incluidos los servicios, pueden registrarse para recibir notificaciones de eventos de dispositivo. Por ejemplo, un servicio de catálogo puede recibir un aviso de los volúmenes que se montan o desmontan, por lo que puede ajustar las rutas de acceso a los archivos del volumen. El sistema notifica a una aplicación que se ha producido un evento de dispositivo mediante el envío de un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) a la aplicación. El sistema notifica a un servicio que se ha producido un evento de dispositivo mediante la invocación de la función de controlador de eventos del servicio, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Para recibir avisos de eventos de dispositivo, llame a la función [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) con una estructura de [**controlador de \_ difusión \_ de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) . Asegúrese de establecer el miembro **de \_ identificador de dbch** en el identificador de dispositivo Obtenido de la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Además, establezca el miembro de **dbch \_ DeviceType** en **DBT \_ DEVTYP \_ Handle**. La función devuelve un identificador de notificación de dispositivo. Tenga en cuenta que esto no es lo mismo que el identificador de volumen.

Cuando la aplicación recibe una notificación, si el tipo de evento es [DBT \_ CUSTOMEVENT](dbt-customevent.md), es posible que haya recibido uno de los eventos de dispositivo definidos en IoEvent. h. Para determinar si se ha producido uno de estos eventos, siga estos pasos.

1.  Trate los datos de evento como una estructura [**\_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Compruebe que el miembro de **dbch \_ DeviceType** está establecido en **DBT \_ DEVTYP \_ Handle**.
2.  Si **dbch \_ DeviceType** es **DBT \_ DEVTYP \_ Handle**, los datos de evento son, en realidad, un puntero a una estructura de [**\_ \_ controlador de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .
3.  Compare el **miembro \_ eventguid de dbch** con los **GUID** que aparecen en la siguiente tabla mediante la función [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**\_ \_ bloqueo exclusivo de CDROM de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



El dispositivo de CD-ROM se ha bloqueado para acceso exclusivo.

**Windows Server 2003 y Windows XP:** La compatibilidad con este valor requiere IMAPi 2,0. Para obtener más información, consulte [Image Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**\_ \_ \_ desbloqueo exclusivo de CDROM de e/s de GUID \_**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Se ha desbloqueado un dispositivo de CD-ROM que estaba bloqueado para acceso exclusivo.

**Windows Server 2003 y Windows XP:** La compatibilidad con este valor requiere IMAPi 2,0. Para obtener más información, consulte [Image Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**el \_ dispositivo de e/s de GUID \_ \_ \_ está listo**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



El proceso de ejecución multimedia está en curso.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ solicitud externa de dispositivo de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Hay varias causas posibles para este evento: para obtener más información, consulte especificación de la especificación de MMC de T10 del comando GET EVENT STATUs NOTIFICATION, en [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_llegada de medios de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Se han agregado medios extraíbles al dispositivo. El miembro de **\_ datos dbch** es un puntero a una estructura de [**contexto de cambio de medios de clase \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . El miembro **NewState** proporciona información de estado. Por ejemplo, un valor de **MediaUnavailable** indica que el medio no está disponible (por ejemplo, debido a una sesión de grabación activa).

**Windows XP:** El miembro de **\_ datos dbch** es un valor **ULong** que representa el número de veces que se ha cambiado el contenido multimedia desde el inicio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_solicitud de \_ \_ expulsión de medios de e/s de GUID \_**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



La unidad del medio extraíble ha recibido una solicitud del usuario para expulsar la ranura o el medio especificado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_eliminación de medios de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Los medios extraíbles se han quitado del dispositivo o no están disponibles. El miembro de **\_ datos dbch** es un puntero a una estructura de [**contexto de cambio de medios de clase \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . El miembro **NewState** proporciona información de estado. Por ejemplo, un valor de **MediaUnavailable** indica que el medio no está disponible (por ejemplo, debido a una sesión de grabación activa).

**Windows XP:** El miembro de **\_ datos dbch** es un valor **ULong** que representa el número de veces que se ha cambiado el contenido multimedia desde el inicio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_cambio de volumen de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



La etiqueta del volumen ha cambiado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_tamaño de \_ cambio de volumen de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



El tamaño del sistema de archivos del volumen ha cambiado.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**Desmontaje del \_ volumen de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Está en curso un intento de desmontar el volumen. Debe cerrar todos los identificadores de los archivos y directorios del volumen. Este evento no estará necesariamente precedido por un evento **de \_ \_ \_ bloqueo de volumen de e/s de GUID** .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ \_ no se pudo desmontar el volumen de e/s de GUID \_**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Error al tratar de desmontar un volumen. Esto suele ocurrir porque otro proceso no pudo responder a un aviso de **\_ \_ \_ desmontaje de volumen de e/s de GUID** cerrando los identificadores pendientes. Dado que se produjo un error al desmontar, puede volver a abrir los identificadores del volumen afectado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_cambio de \_ Estado de FVE de volumen de e/s de \_ \_ GUID \_**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



El estado de Cifrado de unidad BitLocker del volumen ha cambiado. Este evento se señala cuando BitLocker está habilitado o deshabilitado, o cuando se inicia, finaliza, pausa o reanuda el cifrado.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_bloqueo de volumen de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

50708874-c9af-11D1-8fef-00a0c9a06d32
</dt> <dt>



Otro proceso está intentando bloquear el volumen. Debe cerrar todos los identificadores de los archivos y directorios del volumen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_error de \_ bloqueo de volumen de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Error al tratar de bloquear un volumen. Esto suele ocurrir porque otro proceso no pudo responder a un evento de **\_ bloqueo de \_ volumen \_ de e/s de GUID** cerrando los identificadores pendientes. Debido a que se produjo un error en el bloqueo, puede volver a abrir los identificadores del volumen afectado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montaje de volumen de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Otro proceso ha montado el volumen. Puede abrir uno o más identificadores en él.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_cambio de \_ nombre de volumen de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



Se ha cambiado el nombre del volumen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**el \_ volumen de e/s de GUID \_ \_ necesita \_ CHKDSK**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Un sistema de archivos ha detectado daños en el volumen. La aplicación debe ejecutar CHKDSK en el volumen o notificar al usuario que lo haga.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_cambio de \_ \_ configuración física \_ de volumen de e/s de GUID \_**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



Ha cambiado la estructura física o el estado físico actual del volumen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**\_volumen de e/s de GUID \_ preparación de \_ \_ expulsión**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



El sistema de archivos está preparando el disco que se va a expulsar. Por ejemplo, el sistema de archivos está deteniendo una operación de formato en segundo plano o cerrando la sesión en un medio de escritura.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_cambio de \_ \_ identificador único \_ de volumen de e/s de GUID \_**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



Se ha cambiado el identificador único del volumen. Para obtener más información sobre el identificador único, consulte [**ioctl \_ MOUNTDEV \_ query \_ Unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite hasta Windows Server 2008 R2 y Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**desbloqueo del volumen de \_ e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



Otro proceso ha desbloqueado el volumen. Puede abrir uno o más identificadores en él.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**\_volumen de e/s de GUID \_ \_ \_**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



El contenido multimedia se está agotando. Este evento se envía cuando un sistema de archivos determina que la tasa de errores de un volumen es demasiado alta o que el espacio de sustitución del defecto está casi agotado.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los eventos de **\_ \_ \_ \_ error** de desmontaje de volumen de e/s de GUID e e/s de GUID están relacionados, al igual que los eventos de **\_ \_ \_** error de bloqueo de volumen de e/s de GUID e e **\_ /s \_ \_ \_** . **\_ \_ \_** Los eventos de bloqueo de volumen de e/s de GUID e e **\_ /s \_ \_** de GUID indican que se está intentando realizar una operación. **\_ \_ \_** Debe actuar en la notificación de eventos y registrar la acción realizada. Error **de \_ \_ \_ desmontaje \_ de volumen de e** /s de GUID y eventos de **\_ \_ \_ \_ error de bloqueo de volumen de e/s de GUID** indican que se produjo un error en la operación Después, puede usar el registro para deshacer las acciones realizadas en respuesta a la operación.

El miembro **dbch \_ hdevnotify** de la estructura de [**\_ \_ control de difusión de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica el dispositivo afectado. Tenga en cuenta que se trata del identificador de notificación de dispositivo devuelto por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), no por un identificador de volumen. Para realizar operaciones en el volumen, asigne este identificador al identificador de volumen correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>IoEvent. h</dt> </dl> |



 

