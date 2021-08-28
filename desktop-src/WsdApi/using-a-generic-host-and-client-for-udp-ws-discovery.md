---
description: Si el cliente y el host no se pueden ver en la red, se puede sustituir un host y un cliente genéricos por el host personalizado y el cliente para ayudar a solucionar el problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Uso de un host y un cliente genéricos para udp WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b9f42cd76e54c3ee04a3299e9f23eecbfdd73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883073"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Uso de un host y un cliente genéricos para udp WS-Discovery

Si el cliente y el host no se pueden ver en la red, se puede sustituir un host y un cliente genéricos por el host personalizado y el cliente para ayudar a solucionar el problema. Si la dirección del dispositivo no aparece en la salida del cliente de depuración de WSD, el entorno de red probablemente esté causando el error. Para obtener más información sobre el host y el cliente genéricos, vea [Herramientas de depuración](debugging-tools.md).

Si el host o el cliente es una aplicación que se ejecuta en un equipo, el host o el cliente genéricos deben ejecutarse en el mismo contexto de seguridad que el host o cliente real. Por ejemplo, si el host o cliente real se ejecuta como administrador, el host o cliente genérico debe ejecutarse como administrador. Además, si el host o el cliente es un dispositivo independiente, debe reemplazarse completamente por un equipo que ejecute un host o cliente genérico.

**Para usar un host y un cliente genéricos para solucionar problemas de detección de WS de UDP**

1.  Abra una ventana de símbolo del sistema.
2.  Ejecute el siguiente comando: **WSDDebug \_host.exe /mode metadata /start**

    > [!Note]  
    > Puede **Seguridad de Windows cuadro de diálogo** Alerta de alerta. Si es así, haga **clic en Desbloquear** para permitir que se ejecute el host de depuración de WSD.

     

    Este comando genera una salida similar a la siguiente. Anote el identificador del dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Ejecute el siguiente comando: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *&lt; id &gt;*. Reemplace *&lt; id &gt;* por el identificador de dispositivo identificado en el paso 2.
    > [!Note]  
    > Puede **Seguridad de Windows cuadro de diálogo** Alerta de alerta. Si es así, haga **clic en Desbloquear** para permitir que se ejecute el cliente de depuración de WSD.

     

El cliente de depuración de WSD genera una salida similar a la siguiente.

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
```

El cliente de depuración de WSD puede generar una gran cantidad de salidas en una red con muchos dispositivos DPWS. La salida se puede redirigir a un archivo para facilitar el análisis. Escriba **log tee** *&lt; filename en &gt;* el símbolo del sistema del cliente de depuración de WSD para redirigir la salida a un archivo. Para detener el redireccionamiento de salida, escriba **log tee stop** en el símbolo del sistema del cliente de depuración de WSD.

Tome nota de la dirección de referencia de punto de conexión (EPR). Esta dirección EPR debe coincidir con el identificador de dispositivo identificado en el paso 2 anterior. Si este es el caso, es probable que el error de la aplicación no esté relacionado con el sistema operativo o el entorno de red. Reemplace el host y el cliente genéricos por el host y el cliente personalizados, y continúe con la solución de problemas siguiendo los procedimientos descritos en Uso del cliente de depuración [de WSD](using-wsddebug-client-to-verify-multicast-traffic.md)para comprobar el tráfico de multidifusión.

Si el identificador de dispositivo no coincide con la dirección epr, el error de la aplicación probablemente esté relacionado con el sistema operativo o el entorno de red. El error podría tener una o varias de las siguientes causas:

-   La aplicación se ejecuta en el contexto de seguridad incorrecto. Compruebe que la aplicación usa las credenciales correctas y que el cliente y el host tienen permisos suficientes para acceder a la red.
-   La configuración del firewall es incorrecta. Siga las instrucciones de [Inspecting Adapter and Firewall Configuración](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets. El cliente y el host también se pueden copiar en una máquina "con problemas" (una con una instalación de sistema operativo predeterminada que nunca se ha unido a un dominio) para intentar reproducir el error.
-   Una directiva IPSec está bloqueando la aplicación. Copie el cliente y el host en una máquina que no está sujeta a directivas IPSec e intente reproducir el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



