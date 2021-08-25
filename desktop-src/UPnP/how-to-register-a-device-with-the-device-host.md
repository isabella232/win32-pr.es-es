---
title: Cómo registrar un dispositivo con el host de dispositivo
description: Puede registrar un dispositivo en ejecución o un dispositivo que no esté en ejecución.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8425578dbd5ccc76685c2a142bee8d2167c4058341c32e4b03bcedca15041579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867585"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Cómo registrar un dispositivo con el host de dispositivo

Puede registrar un dispositivo en ejecución o un dispositivo que no esté en ejecución.

## <a name="registering-a-running-device"></a>Registro de un dispositivo en ejecución

Los dispositivos se registran mediante [**la interfaz IUPnPRegistrar.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) Solo los administradores pueden registrar dispositivos en ejecución. Para registrar un dispositivo que tiene un objeto de control de dispositivo en ejecución, una aplicación debe invocar [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), pasando lo siguiente:

-   Texto de la descripción del dispositivo.
-   Puntero **IUnknown** al objeto de control de dispositivo.
-   Cadena de inicialización que se pasa al método [**IUPnPPDeviceControl::Initialize del**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) objeto de control de dispositivo.
-   Ubicación del directorio de recursos.
-   Duración del dispositivo.
-   El parámetro Device ID (un parámetro OUT), que es el valor devuelto de esta llamada; Se devuelve un puntero al id. de dispositivo en C++.

## <a name="registering-a-non-running-device"></a>Registro de un dispositivo que no se está ejecutando

De forma predeterminada, solo los administradores y los usuarios interactivos pueden registrar dispositivos que no se ejecutan. Para registrar un dispositivo con un objeto de control de dispositivo que no se está ejecutando, la aplicación usa el [**método IUPnPRegistrar::RegisterDevice.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)

Para registrar un dispositivo mediante programación con un objeto de control de dispositivo que no se está ejecutando, la aplicación debe invocar [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) y pasar los parámetros siguientes:

-   Texto de la descripción del dispositivo.
-   ProgID del objeto de control de dispositivo.
-   Cadena de inicialización que se pasa al método [**IUPnPPDeviceControl::Initialize del**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) objeto de control de dispositivo.
-   Un identificador de contenedor.
-   Ubicación del directorio de recursos.
-   Duración del dispositivo.
-   El parámetro Device ID (un parámetro OUT), que es el valor devuelto de esta llamada; Se devuelve un puntero al id. de dispositivo en C++.

Los registros de dispositivos que no se ejecutan se pueden configurar para que persistan en los arranques del sistema (los dispositivos no se publiquen durante la fase de apagado). Por lo tanto, si se configuran de esta manera, los dispositivos se publican y anuncian cada vez que se inicia el equipo.

 

 




