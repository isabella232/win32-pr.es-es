---
title: Cómo registrar un dispositivo con el host del dispositivo
description: Puede registrar un dispositivo en ejecución o un dispositivo no en ejecución.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075761"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Cómo registrar un dispositivo con el host del dispositivo

Puede registrar un dispositivo en ejecución o un dispositivo no en ejecución.

## <a name="registering-a-running-device"></a>Registro de un dispositivo en ejecución

Los dispositivos se registran mediante la interfaz [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Solo los administradores pueden registrar los dispositivos en ejecución. Para registrar un dispositivo que tiene un objeto de control de dispositivo en ejecución, una aplicación debe invocar [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), pasando lo siguiente:

-   Texto de la descripción del dispositivo.
-   Un puntero **IUnknown** al objeto de control de dispositivo.
-   Una cadena de inicialización que se pasa al método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) del objeto de control de dispositivo.
-   Ubicación del directorio de recursos.
-   La duración del dispositivo.
-   Parámetro de identificador de dispositivo (parámetro de salida), que es el valor devuelto de esta llamada; en C++ se devuelve un puntero al identificador de dispositivo.

## <a name="registering-a-non-running-device"></a>Registro de un dispositivo que no está en ejecución

De forma predeterminada, solo los administradores y los usuarios interactivos pueden registrar dispositivos que no están en ejecución. Para registrar un dispositivo con un objeto de control de dispositivo que no se está ejecutando, la aplicación usa el método [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .

Para registrar un dispositivo mediante programación con un objeto de control de dispositivo que no se está ejecutando, la aplicación debe invocar [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) y pasarle los parámetros siguientes:

-   Texto de la descripción del dispositivo.
-   Identificador de programa (ProgID) del objeto de control de dispositivo.
-   Una cadena de inicialización que se pasa al método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) del objeto de control de dispositivo.
-   IDENTIFICADOR del contenedor.
-   Ubicación del directorio de recursos.
-   La duración del dispositivo.
-   Parámetro de identificador de dispositivo (parámetro de salida), que es el valor devuelto de esta llamada; en C++ se devuelve un puntero al identificador de dispositivo.

Los registros de dispositivos no en ejecución se pueden configurar para que se conserven en los arranques del sistema (los dispositivos no se publican durante la fase de apagado). Por lo tanto, si se configuran de esta manera, los dispositivos se publican y anuncian cada vez que se inicia el equipo.

 

 




