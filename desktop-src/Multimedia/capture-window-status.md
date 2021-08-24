---
title: Estado de la ventana de captura
description: Estado de la ventana de captura
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS mensaje
- CapGetStatus macro
- Capstatus (estructura)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 367d35c3869adb6f4e960fa472e0cd6a22483c37fa981e886b3a78f0b7410029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375291"
---
# <a name="capture-window-status"></a>Estado de la ventana de captura

Puede recuperar el estado actual de una ventana de captura mediante el mensaje [**\_ GET \_ \_ STATUS**](wm-cap-get-status.md) de WM CAP (o la macro [**capGetStatus).**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) Este mensaje recupera una copia de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) con los valores actuales de sus miembros. La **estructura CAPSTATUS** contiene información sobre las dimensiones de la imagen, la posición de desplazamiento y si está habilitada la superposición o la vista previa de la imagen. Dado que la información representada en **CAPSTATUS** es dinámica, la aplicación debe actualizar el contenido de la estructura siempre que el tamaño o el formato de la secuencia de vídeo capturada haya cambiado (por ejemplo, después de mostrar el formato de vídeo del controlador de captura).

Cambiar las dimensiones de la ventana de captura no tiene ningún efecto en las dimensiones de la secuencia de vídeo capturada real. El cuadro de diálogo formato que muestra el controlador de dispositivo de captura de vídeo controla las dimensiones de la secuencia de vídeo capturada.

 

 




