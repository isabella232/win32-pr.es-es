---
title: Acerca de la administración de puertos y servidores RAS
description: Las funciones de administración del servidor RAS obtienen información sobre un servidor RAS especificado y sus puertos. Estas funciones también se usan para finalizar una conexión en un puerto de servidor RAS especificado.
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- RRAS de administración de RAS, administración de puertos y servidores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062773"
---
# <a name="about-ras-server-and-port-administration"></a>Acerca de la administración de puertos y servidores RAS

Las funciones de administración del servidor RAS obtienen información sobre un servidor RAS especificado y sus puertos. Estas funciones también se usan para finalizar una conexión en un puerto de servidor RAS especificado.

La [**función MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) devuelve una estructura [**MPR SERVER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0) que contiene información sobre la configuración de un servidor RAS. La información devuelta incluye el número de puertos disponibles actualmente para las conexiones, el número de puertos actualmente en uso y el número de versión del servidor.

La [**función MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) recupera una matriz de estructuras [**RAS PORT \_ \_ 0.**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) Cada estructura contiene información para uno de los puertos configurados en un servidor RAS. La información de cada puerto incluye:

-   Nombre del puerto
-   Información sobre el dispositivo conectado al puerto
-   Si el servidor RAS asociado al puerto es un servidor Windows NT/Windows 2000 Server
-   Si el puerto está actualmente en uso y, si lo está, información sobre la conexión

Para obtener los puertos que usa una conexión específica, pase [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) un identificador a esa conexión en el *parámetro hConnection.* Para obtener un identificador para una conexión, use la [**función MprAdminConnectionEnum.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) Como alternativa, si ha implementado un archivo DLL de administración de [RAS,](ras-administration-dll.md)las funciones [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) reciben un identificador para cada nueva conexión en el momento en que se establece la conexión.

Puede llamar a la [**función MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) para obtener información adicional sobre un puerto especificado en un servidor RAS. Esta función devuelve una [**estructura \_ RAS PORT \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) que contiene una estructura [**RAS PORT \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e información adicional sobre el estado actual del puerto. La [**función RasAdminPortGetInfo**](rasadminportgetinfo.md) también devuelve una matriz de estructuras [**RAS \_ PARAMETERS**](ras-parameters-str.md) que describen los valores de las claves específicas del medio asociadas al puerto. Una **estructura \_ RAS PARAMETERS** usa un valor de la enumeración RAS [**\_ PARAMS \_ FORMAT**](ras-params-format-str.md) para indicar el formato del valor de cada clave específica del medio.

La [**función MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) también devuelve una estructura [**RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) que contiene varios contadores estadísticos para la conexión actual, si hay alguna, en el puerto. Para un puerto que forma parte de una conexión de varios vínculos, **MprAdminPortGetInfo** devuelve estadísticas para el puerto individual y estadísticas acumulativas para todos los puertos implicados en la conexión. Puede usar la función [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) para restablecer los contadores estadísticos del puerto. La [**función MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) desconecta un puerto que está en uso.

Use la [**función MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) para liberar memoria asignada por las funciones [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) y [**MprAdminPortGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) Use la [**función MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) para obtener una cadena que describa un código de error ras devuelto por una de las funciones de administración del servidor RAS (RasAdmin).

 

 




