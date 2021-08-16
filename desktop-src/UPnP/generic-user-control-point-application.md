---
title: Aplicación genérica de punto de control de usuario
description: La aplicación de punto de control de usuario genérico (UCP) permite detectar dispositivos, controlar esos dispositivos detectados y ver la información de eventos relacionada, todo ello mediante una interfaz gráfica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0bbf454da2bf36becb3c8b0aff2babc87925df7ac658fc9dc7963ba9182fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655744"
---
# <a name="generic-user-control-point-application"></a>Aplicación genérica de punto de control de usuario

La aplicación de punto de control de usuario genérico (UCP) permite detectar dispositivos, controlar esos dispositivos detectados y ver la información de eventos relacionada, todo ello mediante una interfaz gráfica.

**Para iniciar la aplicación UCP genérica**

1.  Cree y configure los ejemplos \\ netds \\ upnp GenericUCP CPPdevtype.txt archivo (o el archivodevtype.txt \\ \\ \\ \\ \\ VisualBasic) con información del dispositivo. Este archivo permite configurar el UCP genérico para las búsquedas "buscar por tipo" y "búsqueda asincrónica". Cada línea del archivo debe contener un tipo de dispositivo y la descripción relacionada. Por ejemplo:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Este ejemplo es para un dispositivo de reproductor multimedia ficticio. La "Media Player" al final de la segunda línea no forma parte del tipo de dispositivo, es para fines informativos en la aplicación UCP genérica. Lo mismo se aplica a "Todos los dispositivos raíz" en la primera línea.

    Agregue una línea que contenga el tipo de dispositivo y la descripción específicos de cada dispositivo.

2.  Cree y configure los ejemplos \\ netds \\ upnp \\ GenericUCP CPPudn.txt file (o el archivoudn.txt VisualBasic) con información de UDN para \\ \\ los \\ \\ dispositivos. Este archivo permite configurar el UCP genérico para la búsqueda "buscar por UDN". Cada línea usa el formato siguiente:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Agregue una línea que contenga el UDN específico para cada dispositivo.

3.  Ejecute GenericUCP.exe. Aparece **la ventana UCP** genérico.

    ![ventana ucp genérica](images/generic-ucp.png)

> [!Note]  
> Visualización **de la presentación** y visualización del servicio **Desc.** no se implementa en el código de ejemplo de C++.

 

 

 




