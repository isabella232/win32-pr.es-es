---
title: Still-Image captura
description: Still-Image captura
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- Mensaje WM_CAP_GRAB_FRAME_NOSTOP
- Mensaje WM_CAP_GRAB_FRAME
- capGrabFrameNoStop (macro)
- capGrabFrame (macro)
- Mensaje WM_CAP_EDIT_COPY
- capEditCopy (macro)
- Mensaje WM_CAP_FILE_SAVEDIB
- capFileSaveDIB (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148787"
---
# <a name="still-image-capture"></a>Still-Image captura

Si quiere capturar un solo fotograma como imagen fija, puede usar [**el mensaje \_ \_ \_**](wm-cap-grab-frame.md) de marco de captura de Cap de WM de la línea de tiempo de almacenamiento, o la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) o [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) , para capturar la imagen digitalizada en un búfer de marco interno. [**\_ \_ \_ \_**](wm-cap-grab-frame-nostop.md) Puede inmovilizar la presentación en la imagen capturada mediante \_ el \_ marco de captación de Cap de WM \_ . De lo contrario, use el \_ marco de captación de Cap de WM \_ \_ \_ .

Una vez capturado, puede copiar la imagen para que la usen otras aplicaciones. Puede copiar una imagen del búfer de fotogramas en el portapapeles mediante el mensaje de edición de Cap de WM (o la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). [**\_ \_ \_**](wm-cap-edit-copy.md) También puede copiar la imagen del búfer de fotogramas en un mapa de bits independiente del dispositivo (DIB) mediante el mensaje [**\_ \_ \_ SAVEDIB del archivo Cap de WM**](wm-cap-file-savedib.md) (o la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ).

La aplicación también puede usar los dos mensajes de captura de un solo fotograma para editar un fotograma de secuencia por fotograma o para crear una secuencia de fotografía de lapso de tiempo.

 

 




