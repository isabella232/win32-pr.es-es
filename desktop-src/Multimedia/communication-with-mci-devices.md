---
title: Comunicación con dispositivos MCI
description: Comunicación con dispositivos MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivos MCI, comunicación
- Macro MCIWndGetDeviceID
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372091"
---
# <a name="communication-with-mci-devices"></a>Comunicación con dispositivos MCI

Cada dispositivo MCI puede usar uno o varios de los siguientes elementos como identificadores:

-   un identificador de dispositivo
-   un nombre de dispositivo
-   un alias
-   el nombre de archivo del contenido cargado actualmente.

MCIWnd proporciona macros que puede usar para recuperar esta información. A continuación, puede usar esta información para comunicarse a través de MCI directamente con dispositivos MCI asociados a ventanas MCIWnd.

Puede recuperar el identificador del dispositivo MCI actual mediante la macro [**MCIWndGetDeviceID.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) El identificador de dispositivo MCI es un valor numérico que identifica la instancia del dispositivo MCI que usa la aplicación. La aplicación puede usar este identificador al comunicarse con un dispositivo MCI mediante la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))

Para recuperar el nombre del dispositivo MCI actual, use la macro [**MCIWndGetDevice.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) El nombre del dispositivo MCI es una cadena terminada en NULL que identifica el tipo de dispositivo asociado a una ventana MCIWnd. La aplicación puede usar este nombre al comunicarse con un dispositivo MCI mediante **mciSendCommand**.

Puede recuperar el alias del dispositivo MCI actual mediante la macro [**MCIWndGetAlias.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) La aplicación puede usar este alias al comunicarse con un dispositivo MCI mediante la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85))

Por último, puede recuperar el nombre de archivo usado por un dispositivo MCI mediante la macro [**MCIWndGetFileName.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) El nombre de archivo identifica el contenido asociado actualmente a una ventana de MCIWnd. La aplicación puede usar este nombre de archivo al comunicarse con un dispositivo MCI mediante **mciSendCommand** o **mciSendString**.

 

 