---
description: Tipos de enumeración usados con administración de discos.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Tipos de enumeración de administración de discos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c186a2a722bf9614bb83b19bcaa29be486cf54bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688290"
---
# <a name="disk-management-enumeration-types"></a>Tipos de enumeración de administración de discos

Los siguientes tipos de enumeración se usan con administración de discos.

## <a name="in-this-section"></a>En esta sección



| Enumeración                                                                              | Descripción                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo de medio \_**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Representa las distintas formas de los medios de dispositivo.<br/>                                                                                                                                                                                                                                                             |
| [**estilo de partición \_**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Representa el formato de una partición.<br/>                                                                                                                                                                                                                                                                     |
| [**\_tipo de bus de almacenamiento \_**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Proporciona un medio simbólico para representar los tipos de bus de almacenamiento.<br/>                                                                                                                                                                                                                                              |
| [**\_Estado de \_ mantenimiento del componente de almacenamiento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Especifica el estado de mantenimiento de un componente de almacenamiento.<br/>                                                                                                                                                                                                                                                       |
| [**\_factor de \_ forma de dispositivo de almacenamiento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Especifica el factor de forma de un dispositivo.<br/>                                                                                                                                                                                                                                                                    |
| [**\_unidades de \_ Cap de energía del dispositivo de almacenamiento \_ \_**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Unidades del umbral de energía máximo.<br/>                                                                                                                                                                                                                                                                 |
| [**\_conjunto de \_ códigos de puerto de almacenamiento \_**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Reservado para uso del sistema. <br/>                                                                                                                                                                                                                                                                                 |
| [**identificador de la propiedad de almacenamiento \_ \_**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Enumera los valores posibles del miembro **PropertyId** de la estructura de [**la \_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) que se pasa como entrada a la solicitud de [**\_ \_ \_ propiedad de consulta de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar las propiedades de un adaptador o dispositivo de almacenamiento.<br/> |
| [**\_tipo de protocolo de almacenamiento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Especifica el protocolo de un dispositivo de almacenamiento.<br/>                                                                                                                                                                                                                                                               |
| [**\_tipo de consulta de almacenamiento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Lo utiliza la estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) que se pasa al código de control de la [**\_ \_ \_ propiedad de consulta de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para indicar qué información se devuelve sobre una propiedad de un adaptador o dispositivo de almacenamiento.<br/>                             |
| [**\_cambio de caché de escritura \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Indica si las características de la memoria caché de escritura de un dispositivo son modificables.<br/>                                                                                                                                                                                                                                    |
| [**\_Habilitar caché de escritura \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Indica si la memoria caché de escritura está habilitada o deshabilitada.<br/>                                                                                                                                                                                                                                                 |
| [**ESCRIBIR \_ tipo de caché \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Especifica el tipo de caché.<br/>                                                                                                                                                                                                                                                                                 |
| [**ESCRITURA \_ a través**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Especifica si un dispositivo de almacenamiento admite el almacenamiento en caché de escritura a través.<br/>                                                                                                                                                                                                                                        |



 

 

