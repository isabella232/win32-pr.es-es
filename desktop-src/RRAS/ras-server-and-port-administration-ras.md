---
title: Administración de puertos y servidores RAS
description: Las funciones de administración del servidor RAS permiten obtener información sobre un servidor RAS especificado y sus puertos. Estas funciones también permiten finalizar una conexión en un puerto de servidor RAS especificado.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d09d683bf0850b5f51a5d9c1ac1aa21b25f2968ddedbed2d383d28dad7785f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028805"
---
# <a name="ras-server-and-port-administration"></a>Administración de puertos y servidores RAS

Las funciones de administración del servidor RAS permiten obtener información sobre un servidor RAS especificado y sus puertos. Estas funciones también permiten finalizar una conexión en un puerto de servidor RAS especificado.

La [**función RasAdminServerGetInfo**](rasadminservergetinfo.md) devuelve una estructura [**RAS SERVER \_ \_ 0**](ras-server-0-str.md) que contiene información sobre la configuración de un servidor RAS. La información devuelta incluye el número de puertos disponibles actualmente para la conexión, el número de puertos actualmente en uso y el número de versión del servidor.

La [**función RasAdminPortEnum**](rasadminportenum.md) recupera una matriz de estructuras [**RAS PORT \_ \_ 0**](ras-port-0-str.md) que contiene información para cada uno de los puertos configurados en un servidor RAS. La información de cada puerto incluye:

-   Nombre del puerto
-   Información sobre el dispositivo conectado al puerto
-   Si el servidor RAS asociado al puerto es un servidor Windows NT/Windows 2000
-   Si el puerto está actualmente en uso y, si lo está, información sobre la conexión

Puede llamar a la [**función RasAdminPortGetInfo**](rasadminportgetinfo.md) para obtener información adicional sobre un puerto especificado en un servidor RAS. Esta función devuelve una estructura [**\_ RAS PORT \_ 1**](ras-port-1-str.md) que contiene una estructura [**RAS PORT \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e información adicional sobre el estado actual del puerto. La **función RasAdminPortGetInfo** también devuelve una matriz de estructuras [**DE PARÁMETROS \_ RAS**](ras-parameters-str.md) que describen los valores de las claves específicas del medio asociadas al puerto. Una **estructura DE PARÁMETROS \_ RAS** usa un valor de la enumeración [**RAS \_ PARAMS \_ FORMAT**](ras-params-format-str.md) para indicar el formato del valor para cada clave específica del medio.

La [**función RasAdminPortGetInfo**](rasadminportgetinfo.md) también devuelve una estructura [**RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) que contiene varios contadores estadísticos para la conexión actual, si hay alguno, en el puerto. Para un puerto que forma parte de una conexión de varios vínculos, **RasAdminPortGetInfo** devuelve estadísticas para el puerto individual y estadísticas acumulativas para todos los puertos implicados en la conexión. Puede usar la [**función RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para restablecer los contadores estadísticos del puerto. La [**función RasAdminPortDisconnect**](rasadminportdisconnect.md) desconecta un puerto que está en uso.

Use la [**función RasAdminFreeBuffer para**](rasadminfreebuffer.md) liberar memoria asignada por las funciones [**RasAdminPortEnum**](rasadminportenum.md) y [**RasAdminPortGetInfo.**](rasadminportgetinfo.md) Use la [**función RasAdminGetErrorString**](rasadmingeterrorstring.md) para obtener una cadena que describa un código de error RAS devuelto por una de las funciones de administración del servidor RAS (RasAdmin).

 

 




