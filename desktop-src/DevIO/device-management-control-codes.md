---
description: Los siguientes códigos de control se usan con dispositivos de cambio.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Administración de dispositivos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164413"
---
# <a name="device-management-control-codes"></a>Administración de dispositivos de control

Los siguientes códigos de control se usan con dispositivos de cambio.



| Value                                                                                          | Significado                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MEDIO DE INTERCAMBIO DE IOCTL \_ CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Mueve un elemento multimedia de un elemento de origen a un destino y el elemento multimedia originalmente en el primer destino a un segundo destino. |
| [**ESTADO DEL ELEMENTO GET DE IOCTL \_ CHANGER \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Recupera el estado de todos los elementos o un número especificado de elementos de un tipo determinado.                                                         |
| [**PARÁMETROS GET DE IOCTL \_ CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Recupera los parámetros del dispositivo especificado.                                                                                                    |
| [**IOCTL \_ CHANGER \_ GET \_ PRODUCT \_ DATA**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Recupera los datos del producto para el dispositivo especificado.                                                                                                 |
| [**ESTADO GET DE IOCTL \_ CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Recupera el estado actual del dispositivo especificado.                                                                                                |
| [**ESTADO DEL ELEMENTO INITIALIZE DE IOCTL \_ CHANGER \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Inicializa el estado de todos los elementos o de los elementos especificados de un tipo determinado.                                                               |
| [**MEDIO DE MOVIMIENTO DE IOCTL \_ CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Mueve un elemento multimedia a un destino.                                                                                                             |
| [**ETIQUETAS DE VOLUMEN DE CONSULTA DE IOCTL \_ CHANGER \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Recupera la información de etiquetas de volumen para los elementos especificados.                                                                                     |
| [**IOCTL \_ CHANGER \_ REINICIALIZA EL \_ TRANSPORTE**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Reequilibra físicamente un elemento de transporte.                                                                                                         |
| [**IOCTL \_ CHANGER \_ SET \_ ACCESS**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Establece el estado del puerto de inserción o expulsión del dispositivo, la puerta o el teclado.                                                                                   |
| [**POSICIÓN DEL \_ CONJUNTO DE CAMBIO \_ DE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Establece el mecanismo de transporte robótico del cambiador en la dirección del elemento especificado.                                                                     |



 

Los siguientes códigos de control se usan con la administración de dispositivos.



| Código de control                                                                                      | Operación                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**COMPROBACIÓN DE \_ ALMACENAMIENTO \_ DE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Comprueba si hay cambios en un dispositivo de medios extraíbles.                                                               |
| [**MEDIOS DE \_ EXPULSIÓN DE ALMACENAMIENTO \_ DE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Expulsa los medios de un dispositivo SCSI.                                                                             |
| [**CONTROL DE \_ EYECCIÓN \_ DE ALMACENAMIENTO DE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Habilita o deshabilita el mecanismo que expulsa los medios.                                                         |
| [**IOCTL \_ STORAGE \_ GET \_ DEVICE \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Recupera el tipo de dispositivo, el número de dispositivo y, para un dispositivo con particiones, el número de partición de un dispositivo. |
| [**IOCTL \_ STORAGE \_ GET \_ HOTPLUG \_ INFO**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Recupera la configuración de hotplug del dispositivo especificado.                                                 |
| [**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ SERIAL \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Recupera el número de serie de un dispositivo USB.                                                                 |
| [**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ TYPES**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Recupera la información de geometría del dispositivo.                                                            |
| [**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ TYPES \_ EX**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Recupera información sobre los tipos de medios admitidos por un dispositivo.                                        |
| [**MEDIOS DE \_ CARGA DE \_ ALMACENAMIENTO DE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Carga medios en un dispositivo.                                                                                   |
| [**ATRIBUTOS DE \_ IOCTL STORAGE \_ MANAGE DATA \_ \_ SET \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**IOCTL \_ STORAGE \_ MCN \_ CONTROL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Habilita o deshabilita la notificación de cambios multimedia.                                                               |
| [**ELIMINACIÓN DE \_ MEDIOS DE ALMACENAMIENTO DE \_ \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Habilita o deshabilita el mecanismo de expulsión de medios.                                                               |
| [**CAPACIDAD DE \_ LECTURA DE \_ ALMACENAMIENTO DE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Recupera la información de geometría del dispositivo.                                                           |
| [**INFORMACIÓN DE \_ HOTPLUG DEL \_ CONJUNTO DE ALMACENAMIENTO \_ DE \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Establece la configuración del hotplug del dispositivo especificado.                                                      |



 

 

 



