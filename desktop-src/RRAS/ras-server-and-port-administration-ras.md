---
title: Administración de puertos y servidores RAS
description: Las funciones de administración del servidor RAS permiten obtener información acerca de un servidor RAS especificado y sus puertos. Estas funciones también permiten terminar una conexión en un puerto de servidor RAS especificado.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af21dfeda38a1c1147bf864a1fa1959092ac946
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075995"
---
# <a name="ras-server-and-port-administration"></a>Administración de puertos y servidores RAS

Las funciones de administración del servidor RAS permiten obtener información acerca de un servidor RAS especificado y sus puertos. Estas funciones también permiten terminar una conexión en un puerto de servidor RAS especificado.

La función [**RasAdminServerGetInfo**](rasadminservergetinfo.md) devuelve una estructura de [**\_ servidor RAS \_ 0**](ras-server-0-str.md) que contiene información sobre la configuración de un servidor RAS. La información devuelta incluye el número de puertos disponibles actualmente para la conexión, el número de puertos actualmente en uso y el número de versión del servidor.

La función [**RasAdminPortEnum**](rasadminportenum.md) recupera una matriz de estructuras del [**Puerto de Ras \_ \_ 0**](ras-port-0-str.md) que contiene información para cada uno de los puertos configurados en un servidor RAS. La información de cada puerto incluye:

-   El nombre del puerto
-   Información sobre el dispositivo conectado al puerto
-   Si el servidor RAS asociado con el puerto es un servidor Windows NT/Windows 2000
-   Si el puerto está en uso y, si es así, la información sobre la conexión

Puede llamar a la función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) para obtener información adicional acerca de un puerto específico en un servidor RAS. Esta función devuelve una estructura de [**\_ Puerto \_ 1 ras**](ras-port-1-str.md) que contiene una estructura del [**Puerto de Ras \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e información adicional sobre el estado actual del puerto. La función **RasAdminPortGetInfo** también devuelve una matriz de estructuras de [**\_ parámetros de Ras**](ras-parameters-str.md) que describen los valores de las claves específicas del medio asociadas al puerto. Una estructura de **\_ parámetros de Ras** usa un valor de la enumeración de [**\_ \_ formato params ras**](ras-params-format-str.md) para indicar el formato del valor de cada clave específica del medio.

La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) también devuelve una estructura de [**\_ \_ estadísticas de Puerto ras**](ras-port-statistics-str.md) que contiene varios contadores de estadísticas para la conexión actual, si hay alguno, en el puerto. En el caso de un puerto que forma parte de una conexión multivínculo, **RasAdminPortGetInfo** devuelve estadísticas para el puerto individual y las Estadísticas acumulativas para todos los puertos implicados en la conexión. Puede usar la función [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para restablecer los contadores de estadísticas para el puerto. La función [**RasAdminPortDisconnect**](rasadminportdisconnect.md) desconecta un puerto que está en uso.

Use la función [**RasAdminFreeBuffer**](rasadminfreebuffer.md) para liberar memoria asignada por las funciones [**RasAdminPortEnum**](rasadminportenum.md) y [**RasAdminPortGetInfo**](rasadminportgetinfo.md) . Utilice la función [**RasAdminGetErrorString**](rasadmingeterrorstring.md) para obtener una cadena que describe un código de error de Ras devuelto por una de las funciones de administración del servidor RAS (RasAdmin).

 

 




