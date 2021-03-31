---
title: Funciones de devolución de llamada ProjFS
description: Las siguientes funciones de devolución de llamada se declaran en projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "103904371"
---
# <a name="callback-functions"></a>Funciones de devolución de llamada

Las siguientes funciones de devolución de llamada se declaran en projectedfslib. h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Notifica al proveedor que se debe cancelar una operación mediante una invocación anterior de una devolución de llamada. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informa al proveedor de que la enumeración de un directorio ha superado. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Solicita información de enumeración de directorio del proveedor.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Solicita el contenido del flujo de datos principal de un archivo.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Solicita información para un archivo o directorio del proveedor.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Entrega las notificaciones al proveedor acerca de las operaciones del sistema de archivos.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Determina si una ruta de acceso de archivo determinada existe en la memoria auxiliar del proveedor.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informa al proveedor de que se está iniciando una enumeración de directorios.