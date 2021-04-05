---
description: Los siguientes códigos de control se usan con dispositivos de cambio.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Códigos de control de administración de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080250"
---
# <a name="device-management-control-codes"></a>Códigos de control de administración de dispositivos

Los siguientes códigos de control se usan con dispositivos de cambio.



| Value                                                                                          | Significado                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cambio \_ medio de \_ intercambio de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Mueve una parte del medio de un elemento de origen a un destino y la parte de los medios originalmente en el primer destino a un segundo destino. |
| [**\_ \_ Estado del elemento get del cambiador de ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Recupera el estado de todos los elementos o un número especificado de elementos de un tipo determinado.                                                         |
| [**\_parámetros GET del cambiador de ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Recupera los parámetros del dispositivo especificado.                                                                                                    |
| [**los \_ datos de producto de los cambiadores de ioctl \_ obtienen \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Recupera los datos del producto para el dispositivo especificado.                                                                                                 |
| [**Estado de la obtención del \_ cambiador de ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Recupera el estado actual del dispositivo especificado.                                                                                                |
| [**\_Estado del \_ elemento de inicialización del cambiador de \_ ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Inicializa el estado de todos los elementos o de los elementos especificados de un tipo determinado.                                                               |
| [**\_movimiento de cambiador de ioctl \_ \_ medio**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Mueve una parte del medio a un destino.                                                                                                             |
| [**\_etiquetas de volumen de consulta de cambiador de ioctl \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Recupera la información de etiqueta de volumen de los elementos especificados.                                                                                     |
| [**\_ \_ reinicialización de transporte del cambiador de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Recalibra físicamente un elemento de transporte.                                                                                                         |
| [**acceso de conjunto de cambios de IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Establece el estado del puerto de inserción/expulsión del dispositivo, la puerta o el teclado numérico.                                                                                   |
| [**posición del conjunto de cambios de IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Establece el mecanismo de transporte de robótica del cambiador en la dirección del elemento especificado.                                                                     |



 

Los siguientes códigos de control se usan con la administración de dispositivos.



| Código de control                                                                                      | Operación                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**comprobación de almacenamiento de IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Comprueba si hay cambios en un dispositivo de medios extraíbles.                                                               |
| [**\_medios de \_ expulsión de almacenamiento ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Expulsa medios de un dispositivo SCSI.                                                                             |
| [**\_control de \_ expulsión de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Habilita o deshabilita el mecanismo que expulsa los elementos multimedia.                                                         |
| [**obtención de un \_ \_ número de \_ dispositivo de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Recupera el tipo de dispositivo, el número de dispositivo y, para un dispositivo particionable, el número de partición de un dispositivo. |
| [**información del almacenamiento de IOCTL \_ \_ Get \_ HOTPLUG \_ info**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Recupera la configuración de hotplug del dispositivo especificado.                                                 |
| [**el \_ almacenamiento ioctl \_ obtiene el número de \_ serie del medio \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Recupera el número de serie de un dispositivo USB.                                                                 |
| [**\_tipos de \_ medios de obtención de almacenamiento de ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Recupera la información de geometría del dispositivo.                                                            |
| [**almacenamiento de IOCTL- \_ \_ obtener \_ tipos de medios \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Recupera información acerca de los tipos de medios admitidos por un dispositivo.                                        |
| [**\_medios de \_ carga de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Carga los archivos multimedia en un dispositivo.                                                                                   |
| [**almacenamiento de IOCTL- \_ \_ administrar \_ atributos de conjunto de datos \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**\_ \_ control MCN de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Habilita o deshabilita la notificación de cambio de medios.                                                               |
| [**\_eliminación de \_ medios de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Habilita o deshabilita el mecanismo de expulsión de medios.                                                               |
| [**\_capacidad de \_ lectura de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Recupera la información de geometría para el dispositivo.                                                           |
| [**\_información de \_ HOTPLUG de conjunto de almacenamiento ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Establece la configuración de hotplug del dispositivo especificado.                                                      |



 

 

 



