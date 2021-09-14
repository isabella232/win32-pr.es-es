---
title: Still-Image capture
description: Still-Image capture
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP mensaje
- WM_CAP_GRAB_FRAME mensaje
- CapGrabFrameNoStop macro
- CapGrabFrame macro
- WM_CAP_EDIT_COPY mensaje
- capEditCopy macro
- WM_CAP_FILE_SAVEDIB mensaje
- capFileSaveDIB macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260836"
---
# <a name="still-image-capture"></a>Still-Image capture

Si desea capturar un único fotograma como imagen fija, puede usar el mensaje [**WM CAP GRAB FRAME \_ \_ \_ \_ NOSTOP**](wm-cap-grab-frame-nostop.md) o [**WM CAP GRAB \_ \_ \_ FRAME**](wm-cap-grab-frame.md) (o la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) o [**capGrabFrame)**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) para capturar la imagen digitalizado en un búfer de fotograma interno. Puede inmovilizar la pantalla en la imagen capturada mediante WM \_ CAP \_ GRAB \_ FRAME. De lo contrario, use WM \_ CAP \_ GRAB FRAME \_ \_ NOSTOP.

Una vez capturada, puede copiar la imagen para que la usen otras aplicaciones. Puede copiar una imagen del búfer de fotogramas al Portapapeles mediante el mensaje [**EDIT \_ \_ \_ COPY**](wm-cap-edit-copy.md) de WM CAP (o la macro [**capEditCopy).**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) También puede copiar la imagen desde el búfer de fotogramas a un mapa de bits independiente del dispositivo (DIB) mediante el mensaje [**\_ \_ \_ SAVEIB**](wm-cap-file-savedib.md) de ARCHIVO CAP DE WM (o la macro [**capFileSaveDIB).**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib)

La aplicación también puede usar los dos mensajes de captura de un solo fotograma para editar un fotograma de secuencia por fotograma, o para crear una secuencia de secuencias de intervalo de tiempo.

 

 




