---
title: Conexión de una ventana de captura a un controlador de captura
description: Conexión de una ventana de captura a un controlador de captura
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT mensaje
- CapDriverConnect (macro)
- Función capGetDriverDescription
- WM_CAP_DRIVER_GET_NAME mensaje
- CapDriverGetName macro
- WM_CAP_DRIVER_GET_VERSION mensaje
- CapDriverGetVersion macro
- WM_CAP_DRIVER_DISCONNECT mensaje
- capDriverDisconnect macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf74b5dc7cda0fdb73c8f9bd73f61de5ecefc157c20816c110d71e04bba6c196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144908"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Conexión de una ventana de captura a un controlador de captura

Puede conectar o desconectar dinámicamente una ventana de captura a un controlador de captura. Puede conectar o asociar una ventana de captura a un controlador de captura mediante el mensaje [**WM \_ CAP DRIVER \_ \_ CONNECT**](wm-cap-driver-connect.md) (o la macro [**capDriverConnect).**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) Después de conectar una ventana de captura y un controlador de captura, puede enviar mensajes específicos del dispositivo al controlador de captura asociado a una ventana de captura.

Si tiene más de un dispositivo de captura instalado en un sistema, puede conectar una ventana de captura a un controlador de dispositivo de captura de vídeo determinado especificando un entero para el parámetro *wParam* del mensaje WM \_ CAP DRIVER \_ \_ CONNECT. El entero es un índice que identifica un controlador de captura de vídeo que aparece en el registro o en la sección de controladores \[ \] del archivo SYSTEM.INI vídeo. Use cero para la primera entrada de índice.

Puede recuperar el nombre y la versión de un controlador de captura instalado mediante la [**función capGetDriverDescription.**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) La aplicación puede usar esta función para enumerar los controladores y dispositivos de captura instalados, de modo que el usuario pueda seleccionar un dispositivo de captura para conectarse a una ventana de captura.

Puede recuperar el nombre del controlador de dispositivo de captura conectado a una ventana de captura mediante el mensaje [**GET \_ \_ \_ \_ NAME**](wm-cap-driver-get-name.md) del CONTROLADOR DE WM CAP (o la macro [**capDriverGetName).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) Para recuperar la versión de un controlador de captura instalado, use el mensaje [**WM CAP DRIVER GET \_ \_ \_ \_ VERSION**](wm-cap-driver-get-version.md) (o la macro [**capDriverGetVersion).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion)

Puede desconectar una ventana de captura de un controlador de captura mediante el mensaje [**WM \_ CAP DRIVER \_ \_ DISCONNECT**](wm-cap-driver-disconnect.md) (o la macro [**capDriverDisconnect).**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)

Cuando se destruye una ventana de captura, los controladores de dispositivos de captura de vídeo conectados se desconectan automáticamente.

 

 




