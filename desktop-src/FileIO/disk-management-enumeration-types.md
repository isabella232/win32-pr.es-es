---
description: Tipos de enumeración usados con la administración de discos.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Tipos de enumeración de administración de discos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e850e5161e4e8a6326d8014f67d6aad9373015e4354a01fa353087c6863a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765915"
---
# <a name="disk-management-enumeration-types"></a>Tipos de enumeración de administración de discos

Los siguientes tipos de enumeración se usan con la administración de discos.

## <a name="in-this-section"></a>En esta sección



| Enumeración                                                                              | Descripción                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ MEDIO**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Representa las distintas formas de medios de dispositivo.<br/>                                                                                                                                                                                                                                                             |
| [**ESTILO DE \_ PARTICIÓN**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Representa el formato de una partición.<br/>                                                                                                                                                                                                                                                                     |
| [**TIPO \_ DE BUS DE \_ ALMACENAMIENTO**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Proporciona un medio simbólico de representar los tipos de bus de almacenamiento.<br/>                                                                                                                                                                                                                                              |
| [**ESTADO DE \_ MANTENIMIENTO DEL COMPONENTE DE \_ \_ ALMACENAMIENTO**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Especifica el estado de mantenimiento de un componente de almacenamiento.<br/>                                                                                                                                                                                                                                                       |
| [**FACTOR DE \_ FORMA DEL DISPOSITIVO DE \_ \_ ALMACENAMIENTO**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Especifica el factor de forma de un dispositivo.<br/>                                                                                                                                                                                                                                                                    |
| [**UNIDADES \_ DE POWER CAP DEL DISPOSITIVO DE \_ \_ \_ ALMACENAMIENTO**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Unidades del umbral de energía máximo.<br/>                                                                                                                                                                                                                                                                 |
| [**CONJUNTO \_ DE CÓDIGO DE PUERTO DE \_ \_ ALMACENAMIENTO**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Reservado para uso del sistema. <br/>                                                                                                                                                                                                                                                                                 |
| [**IDENTIFICADOR \_ DE PROPIEDAD DE \_ ALMACENAMIENTO**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Enumera los valores posibles del miembro **PropertyId** de la estructura [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) pasada como entrada a la solicitud [**IOCTL STORAGE QUERY \_ \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar las propiedades de un adaptador o dispositivo de almacenamiento.<br/> |
| [**TIPO \_ DE PROTOCOLO DE \_ ALMACENAMIENTO**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Especifica el protocolo de un dispositivo de almacenamiento.<br/>                                                                                                                                                                                                                                                               |
| [**TIPO \_ DE CONSULTA DE \_ ALMACENAMIENTO**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Usado por la [**estructura STORAGE \_ PROPERTY \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) pasada al código de control [**IOCTL STORAGE QUERY \_ \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para indicar qué información se devuelve sobre una propiedad de un adaptador o dispositivo de almacenamiento.<br/>                             |
| [**CAMBIO \_ DE CACHÉ DE \_ ESCRITURA**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Indica si las características de caché de escritura de un dispositivo son modificables.<br/>                                                                                                                                                                                                                                    |
| [**HABILITACIÓN \_ DE LA CACHÉ DE \_ ESCRITURA**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Indica si la caché de escritura está habilitada o deshabilitada.<br/>                                                                                                                                                                                                                                                 |
| [**TIPO DE \_ CACHÉ \_ DE ESCRITURA**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Especifica el tipo de caché.<br/>                                                                                                                                                                                                                                                                                 |
| [**ESCRITURA \_ A TRAVÉS**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Especifica si un dispositivo de almacenamiento admite el almacenamiento en caché de escritura a través.<br/>                                                                                                                                                                                                                                        |



 

 

