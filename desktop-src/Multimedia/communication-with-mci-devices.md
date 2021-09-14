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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069545"
---
# <a name="communication-with-mci-devices"></a>Comunicación con dispositivos MCI

Es posible que cada dispositivo MCI use uno o varios de los siguientes elementos como identificadores:

-   un identificador de dispositivo
-   un nombre de dispositivo
-   un alias
-   nombre de archivo del contenido cargado actualmente.

MCIWnd proporciona macros que puede usar para recuperar esta información. A continuación, puede usar esta información para comunicarse a través de MCI directamente con dispositivos MCI asociados a ventanas MCIWnd.

Puede recuperar el identificador del dispositivo MCI actual mediante la macro [**MCIWndGetDeviceID.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) El identificador de dispositivo MCI es un valor numérico que identifica la instancia del dispositivo MCI que usa la aplicación. La aplicación puede usar este identificador al comunicarse con un dispositivo MCI mediante la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))

Para recuperar el nombre del dispositivo MCI actual, use la macro [**MCIWndGetDevice.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) El nombre del dispositivo MCI es una cadena terminada en NULL que identifica el tipo de dispositivo asociado a una ventana MCIWnd. La aplicación puede usar este nombre al comunicarse con un dispositivo MCI mediante **mciSendCommand**.

Puede recuperar el alias del dispositivo MCI actual mediante la macro [**MCIWndGetAlias.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) La aplicación puede usar este alias al comunicarse con un dispositivo MCI mediante la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85))

Por último, puede recuperar el nombre de archivo utilizado por un dispositivo MCI mediante la macro [**MCIWndGetFileName.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) El nombre de archivo identifica el contenido asociado actualmente a una ventana de MCIWnd. La aplicación puede usar este nombre de archivo al comunicarse con un dispositivo MCI mediante **mciSendCommand** o **mciSendString**.

 

 