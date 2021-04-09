---
description: Los registros de WinHTTP se pueden utilizar para ayudar a solucionar problemas de las aplicaciones WSDAPI. Esto resulta útil cuando se produce un error de intercambio de metadatos o cuando se produce un error en la negociación SSL/TLS.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Captura de registros de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155989"
---
# <a name="capturing-winhttp-logs"></a>Captura de registros de WinHTTP

Los registros de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) se pueden utilizar para ayudar a solucionar problemas de las aplicaciones WSDAPI. Esto resulta útil cuando se produce un error de intercambio de metadatos o cuando se produce un error en la negociación SSL/TLS.

Este procedimiento muestra cómo capturar los registros de WinHTTP en el equipo cliente. La aplicación cliente basada en WSDAPI no debe estar en ejecución cuando el registro está habilitado. Si la aplicación cliente se está ejecutando cuando el registro está habilitado, el cliente o el equipo deben reiniciarse antes de WS-Discovery y el tráfico de intercambio de metadatos aparecerá en los registros de WinHTTP.

**Para capturar registros de WinHTTP**

1.  Abra una ventana de símbolo del sistema con privilegios elevados en el equipo cliente.
2.  Ejecute el siguiente comando: **netsh WinHTTP Set Tracing Trace-File-prefix = "C: \\ temp \\ DPWS" LEVEL = verbose Format = ANSI State = Enabled Max-Trace-File-size = 1073741824**

    Este comando habilita el registro de WinHTTP. Todos los archivos de registro se almacenarán en el \\ directorio C: Temp y los nombres de archivo comenzarán con el prefijo DPWS. Se almacenarán al menos 1 GB de archivos de registro.

3.  Si el proceso que usa WinHTTP en el cliente ya se está ejecutando, reinicie el equipo. Por ejemplo, si se usan las API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) , el equipo debe reiniciarse. Las API de detección de funciones llaman a WinHTTP desde dentro de un host de servicio, que puede haberse iniciado ya cuando se habilitó el seguimiento.
4.  Inicie la aplicación cliente basada en WSDAPI. Se puede usar la aplicación que se está depurando o el cliente de depuración WSD.
5.  Reproduzca el error de aplicación.
6.  Finalice la aplicación cliente basada en WSDAPI.
7.  Si el proceso que usa WinHTTP no finaliza con la aplicación cliente, reinicie el equipo. Por ejemplo, si se usan las API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) , el equipo debe reiniciarse.
8.  Ejecute el siguiente comando: **netsh WinHTTP Set Tracing state = disabled**

    Este comando deshabilita el registro de WinHTTP.

9.  Inspeccione los registros de DPWS en C: \\ temp y compruebe que se enviaron las solicitudes y los mensajes necesarios.
10. Si se usa la comunicación de canal seguro (HTTPS), compruebe si hay errores de SSL/TLS.

Una vez capturados los registros de WinHTTP, se pueden examinar los registros para buscar la causa de un error de la aplicación WSDAPI. Tenga en cuenta que el editor de texto que se usa para ver estos registros debe ejecutarse como administrador. Para obtener más información, consulte [uso del registro de WinHTTP para comprobar el tráfico Get](using-winhttp-logging-to-verify-get-traffic.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Uso del registro de WinHTTP para comprobar el tráfico Get](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
