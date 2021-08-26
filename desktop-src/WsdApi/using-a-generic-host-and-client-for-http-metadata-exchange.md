---
description: Si el cliente y el host no pueden intercambiar metadatos, se puede sustituir un host y un cliente genéricos por el host y el cliente personalizados para ayudar a solucionar el problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Uso de un host y un cliente genéricos para metadatos HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6623b39989b613e725fb2103165c825425f20b53a4375d6791aa92cd3b99187
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030085"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Uso de un host y un cliente genéricos para metadatos HTTP Exchange

Si el cliente y el host no pueden intercambiar metadatos, se puede sustituir un host y un cliente genéricos por el host y el cliente personalizados para ayudar a solucionar el problema. Si la dirección del dispositivo o los metadatos del dispositivo no aparecen en la salida del cliente de depuración de WSD, las direcciones de transporte proporcionadas o el entorno de red pueden estar causando el error. Para obtener más información sobre el host y el cliente genéricos, vea [Herramientas de depuración](debugging-tools.md).

Si se ha comprobado que un host y un cliente genéricos pueden completar el intercambio de metadatos de WS-Discovery y HTTP, este procedimiento de diagnóstico se puede omitir y la solución de problemas se puede continuar siguiendo los procedimientos descritos en Uso del registro [winHTTP](using-winhttp-logging-to-verify-get-traffic.md)para comprobar la entrada de tráfico.

Si el host o el cliente es una aplicación que se ejecuta en un equipo, el host o el cliente genéricos deben ejecutarse en el mismo contexto de seguridad que el host o cliente real. Por ejemplo, si el host o cliente real se ejecuta como administrador, el host o cliente genérico debe ejecutarse como administrador. Además, si el host o el cliente es un dispositivo independiente, debe reemplazarse completamente por un equipo que ejecute un host o cliente genérico en un contexto de seguridad que garantice un acceso de red ilimitado (por ejemplo, ejecutándose como administrador).

**Para usar un host y un cliente genéricos para solucionar problemas de intercambio de metadatos HTTP**

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

3.  Ejecute el siguiente comando: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *<id>* . Reemplace *<id>* por el identificador de dispositivo identificado en el paso 2.
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

El cliente de depuración de WSD puede generar una gran cantidad de salida en una red con muchos dispositivos DPWS. La salida se puede redirigir a un archivo para facilitar el análisis. Escriba **log tee en** el símbolo del sistema del cliente de depuración de *<filename>* WSD para redirigir la salida a un archivo. Para detener el redireccionamiento de salida, escriba **log tee stop** en el símbolo del sistema del cliente de depuración de WSD.

Tome nota de la dirección de referencia de punto de conexión (EPR). Esta dirección EPR debe coincidir con el identificador de dispositivo identificado en el paso 2 anterior. Compruebe también que el cliente de depuración de WSD ha impreso completamente los metadatos del dispositivo. Los metadatos del dispositivo comienzan `Metadata for host` por y terminan con `End of metadata` .

Si el identificador de dispositivo y los metadatos del dispositivo aparecen correctamente en la salida del cliente de depuración de WSD, es probable que el error de la aplicación no esté relacionado con las direcciones de transporte proporcionadas, el sistema operativo o el entorno de red. Reemplace el host y el cliente genéricos por el host y el cliente personalizados y siga solucionando problemas siguiendo los procedimientos descritos en Uso del registro [WinHTTP para comprobar obtener tráfico.](using-winhttp-logging-to-verify-get-traffic.md)

Si la dirección del dispositivo y los metadatos del dispositivo no aparecen en la salida del cliente de depuración de WSD, el error podría tener una o varias de las siguientes causas:

-   La dirección de transporte anunciada por el host es incorrecta o tiene un formato incorrecto. El cliente de depuración de WSD intenta obtener los metadatos del dispositivo de la dirección URL proporcionada en el **elemento XAddrs** de un [mensaje ProbeMatches](probematches-message.md) [o ResolveMatches.](resolvematches-message.md) La dirección URL usada para el intercambio de metadatos aparece en la salida del cliente de depuración de WSD, precedida de la frase `Using xAddr` . En el ejemplo siguiente se muestran los XAddrs usados para el intercambio de metadatos en la salida del cliente de depuración de WSD anterior.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Si los XAddrs proporcionados no se ajustan a las reglas de validación de [XAddr](xaddr-validation-rules.md), el cliente de depuración de WSD no puede obtener los metadatos del dispositivo.

-   La aplicación se ejecuta en el contexto de seguridad incorrecto. Compruebe que la aplicación usa las credenciales correctas y que el cliente y el host tienen permisos suficientes para acceder a la red.
-   La configuración del firewall es incorrecta. Siga las instrucciones de [Inspecting Adapter and Firewall Configuración](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets. El cliente y el host también se pueden copiar en una máquina "inerme" (una con una instalación de sistema operativo predeterminada que nunca se ha unido a un dominio) para intentar reproducir el error.
-   Una directiva IPSec está bloqueando la aplicación. Copie el cliente y el host en una máquina que no esté sujeta a directivas IPSec e intente reproducir el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



