---
description: Los registros WinHTTP se pueden usar para ayudar a solucionar problemas de aplicaciones WSDAPI. Esto resulta útil cuando se produce un error en el intercambio de metadatos o cuando se produce un error en la negociación de SSL/TLS.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Captura de registros WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174890"
---
# <a name="capturing-winhttp-logs"></a>Captura de registros WinHTTP

[Los registros WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) se pueden usar para ayudar a solucionar problemas de aplicaciones WSDAPI. Esto resulta útil cuando se produce un error en el intercambio de metadatos o cuando se produce un error en la negociación de SSL/TLS.

Este procedimiento muestra cómo capturar registros WinHTTP en el equipo cliente. La aplicación cliente basada en WSDAPI no debe ejecutarse cuando el registro está habilitado. Si la aplicación cliente se ejecuta cuando el registro está habilitado, el cliente o el equipo deben reiniciarse antes de WS-Discovery y el tráfico de intercambio de metadatos aparecerá en los registros winHTTP.

**Para capturar registros WinHTTP**

1.  Abra una ventana del símbolo del sistema con privilegios elevados en el equipo cliente.
2.  Ejecute el comando siguiente: **netsh winhttp set tracing trace-file-prefix="C: \\ Temp \\ dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**

    Este comando habilita el registro WinHTTP. Todos los archivos de registro se almacenarán en el directorio C: Temp y los nombres de archivo \\ comenzarán con el prefijo dpws. Se almacenarán como máximo 1 GB de archivos de registro.

3.  Si el proceso que usa WinHTTP en el cliente ya se está ejecutando, reinicie el equipo. Por ejemplo, si se [usan](/previous-versions/windows/desktop/fundisc/fd-portal) las API de detección de funciones, se debe reiniciar el equipo. Las API de detección de funciones llaman a WinHTTP desde dentro de un host de servicio, que puede que ya se haya iniciado cuando se ha habilitado el seguimiento.
4.  Inicie la aplicación cliente basada en WSDAPI. Se puede usar la aplicación que se está depurando o el cliente de depuración de WSD.
5.  Reproduzca el error de la aplicación.
6.  Finalice la aplicación cliente basada en WSDAPI.
7.  Si el proceso que usa WinHTTP no finaliza con la aplicación cliente, reinicie el equipo. Por ejemplo, si se [usan](/previous-versions/windows/desktop/fundisc/fd-portal) las API de detección de funciones, se debe reiniciar el equipo.
8.  Ejecute el siguiente comando: **netsh winhttp set tracing state=disabled**

    Este comando deshabilita el registro winHTTP.

9.  Inspeccione los registros de DPWS en C: Temp y compruebe que se enviaron las solicitudes \\ y los mensajes necesarios.
10. Si se usa la comunicación de canal seguro (HTTPS), compruebe si hay errores SSL/TLS.

Una vez capturados los registros WinHTTP, los registros se pueden examinar para buscar la causa de un error de la aplicación WSDAPI. Tenga en cuenta que el editor de texto que se usa para ver estos registros debe ejecutarse como administrador. Para obtener más información, [consulte Uso del registro WinHTTP para comprobar el tráfico de get.](using-winhttp-logging-to-verify-get-traffic.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Uso del registro WinHTTP para comprobar el tráfico de get](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
