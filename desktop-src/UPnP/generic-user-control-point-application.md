---
title: Aplicación de punto de control de usuario genérico
description: La aplicación de punto de control de usuario (UCP) genérico permite detectar dispositivos, controlar esos dispositivos detectados y ver la información de eventos relacionados, todo ello mediante una interfaz gráfica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566591"
---
# <a name="generic-user-control-point-application"></a>Aplicación de punto de control de usuario genérico

La aplicación de punto de control de usuario (UCP) genérico permite detectar dispositivos, controlar esos dispositivos detectados y ver la información de eventos relacionados, todo ello mediante una interfaz gráfica.

**Para iniciar la aplicación de UCP genérica**

1.  Cree y configure el \\ archivo Samples netds \\ UPnP \\ GenericUCP \\ CPP \\devtype.txt (o el \\ archivo dedevtype.txt de VisualBasic \\ ) con la información del dispositivo. Este archivo le permite configurar el UCP genérico para las búsquedas "Buscar por tipo" y "búsqueda asincrónica". Cada línea del archivo debe contener un tipo de dispositivo y la descripción relacionada. Por ejemplo:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Este ejemplo es para un dispositivo de reproductor multimedia ficticio. La "Media Player" al final de la segunda línea no forma parte del tipo de dispositivo, sino con fines informativos en la aplicación de UCP genérica. Lo mismo se aplica a "todos los dispositivos raíz" en la primera línea.

    Agregue una línea que contenga su tipo de dispositivo específico y la descripción de cada dispositivo.

2.  Cree y configure el \\ archivo Samples netds \\ UPnP \\ GenericUCP \\ CPP \\udn.txt (o el \\ archivo deudn.txt de VisualBasic \\ ) con información de UDN para los dispositivos. Este archivo le permite configurar el UCP genérico para la búsqueda "Buscar por UDN". Cada línea utiliza el formato siguiente:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Agregue una línea que contenga su UDN específico para cada dispositivo.

3.  Ejecute GenericUCP.exe. Aparece la ventana de **UCP genérica** .

    ![ventana de UCP genérica](images/generic-ucp.png)

> [!Note]  
> La funcionalidad **ver presentación** y **Ver servicio desc.** no se implementa en el código de ejemplo de C++.

 

 

 




