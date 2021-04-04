---
title: Estado de la ventana de captura
description: Estado de la ventana de captura
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Mensaje WM_CAP_GET_STATUS
- capGetStatus (macro)
- Estructura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076116"
---
# <a name="capture-window-status"></a>Estado de la ventana de captura

Puede recuperar el estado actual de una ventana de captura mediante el mensaje [**de \_ \_ \_ Estado de Cap de WM Get**](wm-cap-get-status.md) (o la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ). Este mensaje recupera una copia de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) con los valores actuales de sus miembros. La estructura **CAPSTATUS** contiene información relacionada con las dimensiones de la imagen, la posición de desplazamiento y si está habilitada la superposición u vista previa de la imagen. Dado que la información representada en **CAPSTATUS** es dinámica, la aplicación debe actualizar el contenido de la estructura cada vez que el tamaño o el formato del flujo de vídeo capturado haya cambiado (por ejemplo, después de mostrar el formato de vídeo del controlador de captura).

Cambiar las dimensiones de la ventana de captura no tiene ningún efecto en las dimensiones de la secuencia de vídeo capturada real. El cuadro de diálogo formato mostrado por el controlador de dispositivo de captura de vídeo controla las dimensiones de la secuencia de vídeo capturada.

 

 




