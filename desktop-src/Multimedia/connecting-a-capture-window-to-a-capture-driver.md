---
title: Conectar una ventana de captura a un controlador de captura
description: Conectar una ventana de captura a un controlador de captura
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Mensaje WM_CAP_DRIVER_CONNECT
- capDriverConnect (macro)
- capGetDriverDescription función)
- Mensaje WM_CAP_DRIVER_GET_NAME
- capDriverGetName (macro)
- Mensaje WM_CAP_DRIVER_GET_VERSION
- capDriverGetVersion (macro)
- Mensaje WM_CAP_DRIVER_DISCONNECT
- capDriverDisconnect (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775691"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Conectar una ventana de captura a un controlador de captura

Puede conectar dinámicamente o desconectar una ventana de captura a un controlador de captura. Puede conectar o asociar una ventana de captura con un controlador de captura mediante el mensaje de conexión de controlador de Cap de WM (o la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ). [**\_ \_ \_**](wm-cap-driver-connect.md) Después de conectar una ventana de captura y un controlador de captura, puede enviar mensajes específicos del dispositivo al controlador de captura asociado a una ventana de captura.

Si tiene más de un dispositivo de captura instalado en un sistema, puede conectar una ventana de captura a un determinado controlador de dispositivo de captura de vídeo especificando un entero para el parámetro *wParam* del mensaje de conexión del controlador de Cap de WM \_ \_ \_ . El entero es un índice que identifica un controlador de captura de vídeo incluido en el registro o en \[ la \] sección de controladores del archivo de SYSTEM.INI. Use cero para la primera entrada de índice.

Puede recuperar el nombre y la versión de un controlador de captura instalado mediante la función [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) . La aplicación puede usar esta función para enumerar los dispositivos y controladores de captura instalados, de modo que el usuario pueda seleccionar un dispositivo de captura para conectarse a una ventana de captura.

Puede recuperar el nombre del controlador de dispositivo de captura conectado a una ventana de captura mediante el uso del [**controlador de Cap de WM \_ \_ \_ Get \_ Name**](wm-cap-driver-get-name.md) Message (o la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ). Para recuperar la versión de un controlador de captura instalado, use el mensaje de [**versión del controlador de Cap de WM \_ \_ \_ Get \_**](wm-cap-driver-get-version.md) (o la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).

Puede desconectar una ventana de captura de un controlador de captura mediante el mensaje de [**\_ \_ \_ desconexión del controlador de Cap de WM**](wm-cap-driver-disconnect.md) (o la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).

Cuando se destruye una ventana de captura, los controladores de dispositivo de captura de vídeo conectados se desconectan automáticamente.

 

 




