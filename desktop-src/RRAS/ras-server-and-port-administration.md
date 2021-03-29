---
title: Acerca de la administración de puertos y servidores RAS
description: Las funciones de administración del servidor RAS obtienen información acerca de un servidor RAS especificado y sus puertos. Estas funciones también se usan para terminar una conexión en un puerto de servidor RAS especificado.
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- Administración de RAS RRAS, administración de servidores y puertos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104487195"
---
# <a name="about-ras-server-and-port-administration"></a>Acerca de la administración de puertos y servidores RAS

Las funciones de administración del servidor RAS obtienen información acerca de un servidor RAS especificado y sus puertos. Estas funciones también se usan para terminar una conexión en un puerto de servidor RAS especificado.

La función [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) devuelve una estructura de [**MPR \_ Server \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0) que contiene información sobre la configuración de un servidor RAS. La información devuelta incluye el número de puertos disponibles actualmente para las conexiones, el número de puertos actualmente en uso y el número de versión del servidor.

La función [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) recupera una matriz de estructuras [**del \_ Puerto \_ 0 de Ras**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) . Cada estructura contiene información de uno de los puertos configurados en un servidor RAS. La información de cada puerto incluye:

-   El nombre del puerto
-   Información sobre el dispositivo conectado al puerto
-   Si el servidor RAS asociado con el puerto es un servidor Windows NT/Windows 2000
-   Si el puerto está en uso y, si es así, información sobre la conexión

Para obtener los puertos que usa una conexión específica, pase [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) un identificador a esa conexión en el parámetro *hConnection* . Para obtener un identificador de una conexión, utilice la función [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) . Como alternativa, si ha implementado un [archivo dll de administración de Ras](ras-administration-dll.md), las funciones [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) reciben un identificador para cada nueva conexión en el momento en que se establece la conexión.

Puede llamar a la función [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) para obtener información adicional acerca de un puerto específico en un servidor RAS. Esta función devuelve una estructura de [**\_ Puerto \_ 1 ras**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) que contiene una estructura del [**Puerto de Ras \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e información adicional sobre el estado actual del puerto. La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) también devuelve una matriz de estructuras de [**\_ parámetros de Ras**](ras-parameters-str.md) que describen los valores de las claves específicas del medio asociadas al puerto. Una estructura de **\_ parámetros de Ras** usa un valor de la enumeración de [**\_ \_ formato params ras**](ras-params-format-str.md) para indicar el formato del valor de cada clave específica del medio.

La función [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) también devuelve una estructura de [**\_ \_ estadísticas de Puerto ras**](ras-port-statistics-str.md) que contiene varios contadores de estadísticas para la conexión actual, si hay alguno, en el puerto. En el caso de un puerto que forma parte de una conexión multivínculo, **MprAdminPortGetInfo** devuelve estadísticas para el puerto individual y las Estadísticas acumulativas para todos los puertos implicados en la conexión. Puede usar la función [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) para restablecer los contadores de estadísticas para el puerto. La función [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) desconecta un puerto que está en uso.

Use la función [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) para liberar memoria asignada por las funciones [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) y [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) . Utilice la función [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) para obtener una cadena que describe un código de error de Ras devuelto por una de las funciones de administración del servidor RAS (RasAdmin).

 

 




