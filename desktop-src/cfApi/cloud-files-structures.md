---
description: Las estructuras siguientes se usan para crear y mantener directorios y archivos de marcador de posición.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Estructuras de filtro de nube
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6da8cf5e512c6e65e88d17c5904fca264c28829dd0a0e842227da4b069aa82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130227"
---
# <a name="cloud-filter-structures"></a>Estructuras de filtro de nube

Las estructuras siguientes se usan para crear y mantener directorios y archivos de marcador de posición.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMACIÓN DE \_ DEVOLUCIÓN DE LLAMADA DE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contiene información de devolución de llamada común.<br/>                                                                                          |
| [**PARÁMETROS DE \_ DEVOLUCIÓN DE LLAMADA DE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contiene parámetros específicos de devolución de llamada, como desplazamiento de archivo, longitud, marcas, etc.<br/>                                                 |
| [**REGISTRO DE \_ DEVOLUCIÓN DE LLAMADA DE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Devoluciones de llamada que va a registrar el proveedor de sincronización.<br/>                                                                           |
| [**INTERVALO \_ DE ARCHIVOS CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Especifica un intervalo de datos en un archivo de marcador de posición.<br/>                                                                               |
| [**BÚFER DE \_ INTERVALO \_ DE ARCHIVOS \_ CF**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Estructura para describir la ubicación y el intervalo de datos de un archivo.<br/>                                                              |
| [**METADATOS DE CF \_ FS \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Metadatos de directorio o archivo de marcador de posición.<br/>                                                                                        |
| [**DIRECTIVA \_ DE HIDRATACIÓN DE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Especifica la directiva de hidratación principal y su modificador .<br/>                                                                       |
| [**INFORMACIÓN DE OPERACIÓN DE CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Información sobre una operación en un archivo o carpeta de marcador de posición.<br/>                                                                |
| [**PARÁMETROS DE OPERACIÓN DE CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parámetros de una operación en un archivo o carpeta de marcador de posición.<br/>                                                                    |
| [**INFORMACIÓN BÁSICA \_ DEL MARCADOR DE POSICIÓN \_ \_ DE CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Información básica del marcador de posición.<br/>                                                                                                 |
| [**INFORMACIÓN DE \_ CREACIÓN DE MARCADOR DE POSICIÓN \_ DE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contiene información de marcador de posición para crear nuevos archivos o directorios de marcador de posición. <br/>                                           |
| [**CF \_ PLACEHOLDER \_ STANDARD \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Información de marcador de posición estándar.<br/>                                                                                              |
| [**CF \_ PLATFORM \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Devuelve información para la plataforma de archivos en la nube. Está pensado para proveedores de sincronización que se ejecutan en varias versiones de Windows.<br/> |
| [**DIRECTIVA \_ DE POBLACIÓN DE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Especifica la directiva de población principal y su modificador .<br/>                                                                      |
| [**INFORMACIÓN DEL PROCESO DE CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contiene información sobre un proceso de usuario.<br/>                                                                                     |
| [**DIRECTIVAS DE SINCRONIZACIÓN DE CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Define las directivas de sincronización utilizadas por una raíz de sincronización.<br/>                                                                                 |
| [**REGISTRO DE SINCRONIZACIÓN DE CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Detalles del proveedor de sincronización y la raíz de sincronización que se va a registrar.<br/>                                                               |
| [**CF \_ SYNC \_ ROOT \_ BASIC \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Información básica de la raíz de sincronización.<br/>                                                                                                   |
| [**INFORMACIÓN DEL \_ \_ PROVEEDOR RAÍZ \_ DE \_ CF SYNC**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Sincronice la información del proveedor raíz.<br/>                                                                                                |
| [**CF \_ SYNC \_ ROOT \_ STANDARD \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Información raíz de sincronización estándar.<br/>                                                                                                |
| [**ESTADO DE SINCRONIZACIÓN DE CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Se usa en una [**estructura CF \_ OPERATION \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) para describir el estado de una raíz de sincronización especificada.<br/>     |



 

 

