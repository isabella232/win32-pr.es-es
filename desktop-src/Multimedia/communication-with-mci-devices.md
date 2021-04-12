---
title: Comunicación con dispositivos MCI
description: Comunicación con dispositivos MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivos MCI, comunicarse
- MCIWndGetDeviceID (macro)
- mciSendCommand función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358832"
---
# <a name="communication-with-mci-devices"></a>Comunicación con dispositivos MCI

Es posible que cada dispositivo MCI utilice uno o varios de los siguientes identificadores:

-   un identificador de dispositivo
-   un nombre de dispositivo
-   un alias
-   nombre de archivo del contenido cargado actualmente.

MCIWnd proporciona macros que puede usar para recuperar esta información. Después, puede usar esta información para comunicarse a través de MCI directamente con dispositivos MCI asociados a MCIWnd Windows.

Puede recuperar el identificador del dispositivo MCI actual mediante la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) . El identificador de dispositivo MCI es un valor numérico que identifica la instancia del dispositivo MCI que está usando la aplicación. La aplicación puede usar este identificador al comunicarse con un dispositivo MCI mediante la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

Para recuperar el nombre del dispositivo MCI actual, use la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) . El nombre del dispositivo MCI es una cadena terminada en null que identifica el tipo de dispositivo asociado a una ventana de MCIWnd. La aplicación puede usar este nombre al comunicarse con un dispositivo MCI mediante **mciSendCommand**.

Puede recuperar el alias del dispositivo MCI actual mediante la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) . La aplicación puede usar este alias al comunicarse con un dispositivo MCI mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .

Por último, puede recuperar el nombre de archivo usado por un dispositivo MCI mediante la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) . El nombre de archivo identifica el contenido asociado actualmente a una ventana de MCIWnd. La aplicación puede usar este nombre de archivo al comunicarse con un dispositivo MCI mediante **mciSendCommand** o **mciSendString**.

 

 