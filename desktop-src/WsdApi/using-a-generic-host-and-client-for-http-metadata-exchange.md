---
description: Si el cliente y el host no pueden intercambiar metadatos, un host y un cliente genéricos se pueden sustituir por el host personalizado y el cliente para ayudar a solucionar el problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Usar un host y un cliente genéricos para el intercambio de metadatos HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705877"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Usar un host y un cliente genéricos para el intercambio de metadatos HTTP

Si el cliente y el host no pueden intercambiar metadatos, un host y un cliente genéricos se pueden sustituir por el host personalizado y el cliente para ayudar a solucionar el problema. Si la dirección del dispositivo o los metadatos del dispositivo no aparecen en la salida del cliente de depuración de WSD, las direcciones de transporte proporcionadas o el entorno de red pueden estar causando el error. Para obtener más información sobre el host y el cliente genéricos, vea [herramientas de depuración](debugging-tools.md).

Si se ha comprobado que un host y un cliente genéricos pueden completar el intercambio de metadatos de WS-Discovery y HTTP, se puede omitir este procedimiento de diagnóstico y se puede continuar con la solución de problemas siguiendo los procedimientos que se describen en [uso del registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).

Si el host o el cliente es una aplicación que se ejecuta en un equipo, el host o el cliente genéricos deben ejecutarse en el mismo contexto de seguridad que el host o cliente real. Por ejemplo, si el host o cliente real se ejecuta como administrador, el host o el cliente genéricos se deben ejecutar como administrador. Además, si el host o el cliente es un dispositivo independiente, debe reemplazarse por completo por un equipo que ejecute un host o un cliente genéricos en un contexto de seguridad que garantice un acceso ilimitado a la red (por ejemplo, en ejecución como administrador).

**Para usar un host y un cliente genéricos para solucionar problemas de intercambio de metadatos HTTP**

1.  Abra una ventana de símbolo del sistema.
2.  Ejecute el comando siguiente: **WSDDebug \_host.exe/Mode Metadata/Start**

    > [!Note]  
    > Puede aparecer un cuadro de diálogo **alerta de seguridad de Windows** . Si es así, haga clic en **desbloquear** para permitir la ejecución del host de depuración de WSD.

     

    Este comando genera un resultado similar al siguiente. Anote el identificador del dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Ejecute el siguiente comando: **WSDDebug \_client.exe/Mode Metadata/Hello OFF/Resolve** *<id>* . Reemplace *<id>* por el identificador de dispositivo identificado en el paso 2.
    > [!Note]  
    > Puede aparecer un cuadro de diálogo **alerta de seguridad de Windows** . Si es así, haga clic en **desbloquear** para permitir que se ejecute el cliente de depuración de WSD.

     

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
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

El cliente de depuración de WSD puede generar una gran cantidad de resultados en una red con muchos dispositivos DPWS. La salida se puede redirigir a un archivo para un análisis más sencillo. Escriba **log Tee** *<filename>* en el mensaje del cliente de depuración WSD para redirigir la salida a un archivo. La redirección de salida se puede detener escribiendo **log Tee STOP** en el símbolo del sistema de depuración WSD.

Tome nota de la dirección de referencia de extremo (EPR). Esta dirección de EPR debe coincidir con el identificador de dispositivo identificado en el paso 2 anterior. Además, compruebe que el cliente de depuración de WSD imprimió por completo los metadatos del dispositivo. Los metadatos del dispositivo comienzan por `Metadata for host` y terminan con `End of metadata` .

Si el identificador de dispositivo y los metadatos del dispositivo aparecen correctamente en la salida del cliente de depuración de WSD, es probable que el error de aplicación no esté relacionado con las direcciones de transporte proporcionadas, el sistema operativo o el entorno de red. Reemplace el host y el cliente genéricos con el cliente y el host personalizados y siga los procedimientos que se indican en [uso del registro de WinHTTP para comprobar el tráfico](using-winhttp-logging-to-verify-get-traffic.md).

Si la dirección del dispositivo y los metadatos del dispositivo no aparecen en la salida del cliente de depuración de WSD, el error podría tener una o varias de las causas siguientes:

-   La dirección de transporte anunciada por el host es incorrecta o tiene un formato incorrecto. El cliente de depuración de WSD intenta obtener los metadatos del dispositivo de la dirección URL proporcionada en el elemento **XAddrs** de un mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) . La dirección URL usada para el intercambio de metadatos aparece en la salida del cliente de depuración WSD, precedida por la frase `Using xAddr` . En el ejemplo siguiente se muestra el XAddrs que se usa para el intercambio de metadatos en la salida del cliente de depuración WSD anterior.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Si el XAddrs proporcionado no se ajusta a las [reglas de validación de XAddr](xaddr-validation-rules.md), el cliente de depuración de WSD no puede obtener los metadatos del dispositivo.

-   La aplicación se está ejecutando en un contexto de seguridad incorrecto. Compruebe que la aplicación está usando las credenciales correctas y que el cliente y el host tienen permisos suficientes para tener acceso a la red.
-   La configuración del Firewall es incorrecta. Siga las instrucciones de [inspección de la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md) para comprobar que la configuración del firewall de Windows sea correcta y que no haya otras reglas que quiten los paquetes. El cliente y el host también se pueden copiar en un equipo "original" (uno con una instalación de sistema operativo predeterminada que nunca se ha unido a un dominio) para intentar reproducir el error.
-   Una directiva IPSec está bloqueando la aplicación. Copie el cliente y el host en un equipo que no esté sujeto a directivas IPSec y trate de reproducir el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



