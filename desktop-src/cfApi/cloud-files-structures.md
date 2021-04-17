---
description: Las siguientes estructuras se utilizan para crear y mantener archivos de marcadores de posición y directorios.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Estructuras de filtro de nube
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659777"
---
# <a name="cloud-filter-structures"></a>Estructuras de filtro de nube

Las siguientes estructuras se utilizan para crear y mantener archivos de marcadores de posición y directorios.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_información de devolución de llamada CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contiene información de devolución de llamada común.<br/>                                                                                          |
| [**\_parámetros de devolución de llamada CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contiene parámetros específicos de devolución de llamada, como desplazamiento de archivos, longitud, marcas, etc.<br/>                                                 |
| [**\_registro de devolución de llamada CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Las devoluciones de llamada que va a registrar el proveedor de sincronización.<br/>                                                                           |
| [**\_intervalo de archivos CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Especifica un intervalo de datos en un archivo de marcador de posición.<br/>                                                                               |
| [**\_búfer de \_ intervalo de archivos CF \_**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Estructura para describir la ubicación y el rango de datos de un archivo.<br/>                                                              |
| [**metadatos de CF \_ FS \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Archivo de marcador de posición o metadatos de directorio.<br/>                                                                                        |
| [**Directiva de la \_ hidratación de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Especifica la Directiva de hidratación principal y su modificador.<br/>                                                                       |
| [**información de la \_ operación CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Información sobre una operación en un archivo o carpeta de marcadores de posición.<br/>                                                                |
| [**parámetros de la \_ operación CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parámetros de una operación en un archivo o carpeta de marcador de posición.<br/>                                                                    |
| [**\_información básica del marcador de posición CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Información básica del marcador de posición.<br/>                                                                                                 |
| [**marca de \_ marcador CF \_ crear \_ información**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contiene información de marcadores de posición para crear nuevos archivos de marcadores de posición o directorios. <br/>                                           |
| [**\_información estándar del marcador de posición CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Información estándar del marcador de posición.<br/>                                                                                              |
| [**\_información de plataforma CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Devuelve información para la plataforma de archivos en la nube. Esto está pensado para los proveedores de sincronización que se ejecutan en varias versiones de Windows.<br/> |
| [**\_Directiva de población de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Especifica la Directiva de rellenado principal y su modificador.<br/>                                                                      |
| [**\_información del proceso de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contiene información acerca de un proceso de usuario.<br/>                                                                                     |
| [**\_directivas de sincronización de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Define las directivas de sincronización usadas por una raíz de sincronización.<br/>                                                                                 |
| [**\_registro de sincronización de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Los detalles del proveedor de sincronización y la raíz de sincronización que se van a registrar.<br/>                                                               |
| [**\_ \_ \_ información básica de la raíz de sincronización de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Información raíz básica de la sincronización.<br/>                                                                                                   |
| [**\_información del \_ \_ proveedor raíz de sincronización \_ de CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Sincronizar la información del proveedor raíz.<br/>                                                                                                |
| [**\_información del \_ \_ estándar raíz de sincronización \_ de CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Información de la raíz de sincronización estándar.<br/>                                                                                                |
| [**\_Estado de sincronización de CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Se usa en una estructura de [**\_ \_ información de la operación CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) para describir el estado de una raíz de sincronización especificada.<br/>     |



 

 

