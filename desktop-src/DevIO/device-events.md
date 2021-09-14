---
description: Las aplicaciones, incluidos los servicios, pueden registrarse para recibir notificaciones de eventos de dispositivo.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Eventos de dispositivo (IoEvent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164433"
---
# <a name="device-events-ioeventh"></a>Eventos de dispositivo (IoEvent.h)

Las aplicaciones, incluidos los servicios, pueden registrarse para recibir notificaciones de eventos de dispositivo. Por ejemplo, un servicio de catálogo puede recibir un aviso de volúmenes montados o desmontados para que pueda ajustar las rutas de acceso a los archivos del volumen. El sistema notifica a una aplicación que se ha producido un evento de dispositivo enviando a la aplicación [**un mensaje DE WM \_ DEVICECHANGE.**](wm-devicechange.md) El sistema notifica a un servicio que se ha producido un evento de dispositivo mediante la invocación de la función de controlador de eventos del servicio, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Para recibir avisos de eventos de dispositivo, llame a [**la función RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) con una estructura [**\_ DEV BROADCAST \_ HANDLE.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) Asegúrese de establecer el miembro **de identificador dbch \_** en el identificador de dispositivo obtenido de la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Además, establezca el **miembro dbch \_ devicetype** en **DBT \_ DEVTYP \_ HANDLE**. La función devuelve un identificador de notificación de dispositivo. Tenga en cuenta que esto no es lo mismo que el identificador de volumen.

Cuando la aplicación recibe una notificación, si el tipo de evento es [DBT \_ CUSTOMEVENT,](dbt-customevent.md)es posible que haya recibido uno de los eventos de dispositivo definidos en IoEvent.h. Para determinar si se ha producido uno de estos eventos, siga estos pasos.

1.  Trate los datos del evento como una [**estructura \_ BROADCAST HDR \_ de DEV.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Compruebe que el **miembro dbch \_ devicetype** está establecido en **DBT \_ DEVTYP \_ HANDLE**.
2.  Si **dbch \_ devicetype** es **DBT \_ DEVTYP \_ HANDLE**, los datos del evento son realmente un puntero a una estructura [**\_ DEV BROADCAST \_ HANDLE.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)
3.  Compare el **miembro dbch \_ eventguid** con los **GUID** enumerados en la tabla siguiente mediante la [**función IsEqualGUID.**](/windows/win32/api/guiddef/nf-guiddef-isequalguid)

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**BLOQUEO \_ EXCLUSIVO \_ DE CDROM DE E/S \_ \_ GUID**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



El dispositivo CD-ROM se ha bloqueado para un acceso exclusivo.

**Windows Server 2003 y Windows XP:** La compatibilidad con este valor requiere IMAPI 2.0. Para obtener más información, vea [Image Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**DESBLOQUEO \_ EXCLUSIVO DE GUID IO \_ CDROM \_ \_**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Se ha desbloqueado un dispositivo CD-ROM bloqueado para acceso exclusivo.

**Windows Server 2003 y Windows XP:** La compatibilidad con este valor requiere IMAPI 2.0. Para obtener más información, vea [Image Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**PREPARAR \_ EL DISPOSITIVO DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



El "spin-up" multimedia está en curso.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**SOLICITUD EXTERNA \_ DE \_ DISPOSITIVO DE \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Hay varias causas posibles de este evento; Para obtener más información, consulte la especificación mmc T10 del comando GET EVENT STATUS NOTIFICATION, en [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**LLEGADA DE \_ MEDIOS DE \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Se han agregado medios extraíbles al dispositivo. El **miembro de \_ datos dbch** es un puntero a una [**estructura CLASS MEDIA CHANGE \_ \_ \_ CONTEXT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) El **miembro NewState** proporciona información de estado. Por ejemplo, un valor de **MediaUnavailable** indica que el medio no está disponible (por ejemplo, debido a una sesión de grabación activa).

**Windows XP:** El **miembro de \_ datos dbch** es un **valor ULONG** que representa el número de veces que se ha cambiado el medio desde el inicio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**SOLICITUD DE \_ EXPULSIÓN \_ DE MEDIOS DE \_ \_ E/S GUID**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



La unidad del medio extraíble ha recibido una solicitud del usuario para expulsar la ranura o el medio especificados.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**ELIMINACIÓN DE \_ MEDIOS \_ DE \_ E/S GUID**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Los medios extraíbles se han quitado del dispositivo o no están disponibles. El **miembro de \_ datos dbch** es un puntero a una [**estructura CLASS MEDIA CHANGE \_ \_ \_ CONTEXT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) El **miembro NewState** proporciona información de estado. Por ejemplo, un valor de **MediaUnavailable** indica que el medio no está disponible (por ejemplo, debido a una sesión de grabación activa).

**Windows XP:** El **miembro de \_ datos dbch** es un **valor ULONG** que representa el número de veces que se ha cambiado el medio desde el inicio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**CAMBIO \_ DE VOLUMEN DE \_ \_ E/S GUID**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



La etiqueta del volumen ha cambiado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**CAMBIO \_ DE TAMAÑO DEL VOLUMEN DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



El tamaño del sistema de archivos del volumen ha cambiado.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**\_DESMONT DEL VOLUMEN DE \_ \_ E/S GUID**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Hay un intento de desmontar el volumen en curso. Debe cerrar todos los identificadores a los archivos y directorios del volumen. Este evento no va a ir precedido necesariamente de un evento **GUID \_ IO VOLUME \_ \_ LOCK.**


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**ERROR \_ DE \_ DESMONTAJE \_ DEL VOLUMEN DE E/S \_ GUID**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Error al tratar de desmontar un volumen. Esto suele ocurrir porque otro proceso no pudo responder a un aviso **DE \_ DESMONT DEL VOLUMEN DE \_ \_ E/S** GUID al cerrar sus identificadores pendientes. Dado que el desmontaje no se pudo desmontar, puede volver a abrir los identificadores en el volumen afectado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**CAMBIO \_ DE ESTADO DE \_ \_ FVE DEL VOLUMEN DE E/S \_ \_ GUID**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cjunto9a6da
</dt> <dt>



El estado de Cifrado de unidad BitLocker del volumen ha cambiado. Este evento se señala cuando BitLocker está habilitado o deshabilitado, o cuando el cifrado comienza, finaliza, se pausa o se reanuda.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**BLOQUEO DE \_ VOLUMEN \_ DE \_ E/S GUID**
</dt> <dd> <dl> <dt>

50708874-c9af-11d1-8fef-00a0c9a06d32
</dt> <dt>



Otro proceso está intentando bloquear el volumen. Debe cerrar todos los identificadores a los archivos y directorios del volumen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**ERROR \_ DE BLOQUEO DE VOLUMEN DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Error al intentar bloquear un volumen. Esto suele ocurrir porque otro proceso no pudo responder a un evento **GUID \_ IO VOLUME \_ \_ LOCK** cerrando sus identificadores pendientes. Dado que se ha producir un error en el bloqueo, puede volver a abrir los identificadores en el volumen afectado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**MONTAJE DEL \_ VOLUMEN \_ DE \_ E/S GUID**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Otro proceso ha montado el volumen. Puede abrir uno o varios identificadores.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**CAMBIO \_ DEL NOMBRE DEL VOLUMEN DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



Se ha cambiado el nombre del volumen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**EL \_ VOLUMEN \_ DE \_ E/S GUID NECESITA \_ CHKDSK**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Un sistema de archivos ha detectado daños en el volumen. La aplicación debe ejecutar CHKDSK en el volumen o notificar al usuario que lo haga.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**CAMBIO DE \_ CONFIGURACIÓN FÍSICA DEL VOLUMEN DE \_ \_ E/S \_ \_ GUID**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



El estado físico o físico actual del volumen ha cambiado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**EXPULSIÓN \_ DE PREPARACIÓN DEL VOLUMEN DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



El sistema de archivos prepara el disco para expulsarlo. Por ejemplo, el sistema de archivos está deteniendo una operación de formato en segundo plano o cerrando la sesión en medios de una escritura.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**CAMBIO DE \_ IDENTIFICADOR ÚNICO DEL VOLUMEN DE \_ \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



Se ha cambiado el identificador único del volumen. Para obtener más información sobre el identificador único, vea [**IOCTL \_ MOUNTDEV \_ QUERY UNIQUE \_ \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Server 2008 R2 y Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**DESBLOQUEO \_ DEL VOLUMEN DE \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



Otro proceso ha desbloqueado el volumen. Puede abrir uno o varios identificadores.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**SALIDA \_ DEL VOLUMEN DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaaa
</dt> <dt>



Los medios se están desabando. Este evento se envía cuando un sistema de archivos determina que la tasa de errores de un volumen es demasiado alta o que casi se agota su espacio de reemplazo de defectos.

**Windows Server 2003 y Windows XP:** Este valor no se admite.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los **eventos GUID IO VOLUME \_ \_ \_ DISMOUNT** y **GUID IO VOLUME \_ \_ \_ DISMOUNT \_ FAILED** están relacionados, al igual que el evento GUID **IO VOLUME \_ \_ \_ LOCK** y **GUID IO VOLUME LOCK \_ \_ \_ \_ FAILED.** Los **eventos GUID IO VOLUME \_ \_ \_ DISMOUNT** y **GUID IO VOLUME \_ \_ \_ LOCK** indican que se está intentando realizar una operación. Debe actuar sobre la notificación de eventos y registrar la acción realizada. Los **eventos GUID IO VOLUME \_ \_ \_ DISMOUNT FAILED \_ y** **GUID IO VOLUME LOCK \_ \_ \_ \_ FAILED** indican que se ha intentado realizar la operación. A continuación, puede usar el registro para deshacer las acciones que realizó en respuesta a la operación.

El **miembro dbch \_ hdevnotify** de la estructura [**BROADCAST \_ \_ HANDLE de DEV**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica el dispositivo afectado. Tenga en cuenta que este es el identificador de notificación de dispositivo devuelto por [**RegisterDeviceNotification,**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)no un identificador de volumen. Para realizar operaciones en el volumen, asigne este identificador al identificador de volumen correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>IoEvent.h</dt> </dl> |



 

