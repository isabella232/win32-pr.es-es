---
title: WM_CAP_DLG_VIDEOCOMPRESSION mensaje (Vfw.h)
description: El mensaje \_ WM CAP \_ DLG VIDEOCOMPRESSION muestra un cuadro de diálogo en el que el usuario puede seleccionar un comentario para usarlo \_ durante el proceso de captura.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816aeb26455ba375b4446edc275ec4fbaa318b67b1fea64bd6049760f45d8235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135448"
---
# <a name="wm_cap_dlg_videocompression-message"></a>Mensaje \_ WM CAP \_ DLG \_ VIDEOCOMPRESSION

El **mensaje WM CAP \_ \_ DLG \_ VIDEOCOMPRESSION** muestra un cuadro de diálogo en el que el usuario puede seleccionar un comentario para usarlo durante el proceso de captura. La lista de dispositivos disponibles puede variar con el formato de vídeo seleccionado en el cuadro de diálogo Formato de vídeo del controlador de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoCompression.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression)


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Comentarios

Use este mensaje con controladores de captura que proporcionen fotogramas solo en el \_ formato RGB de BI. Este mensaje es muy útil en la operación de captura de pasos para combinar la captura y la compresión en una sola operación. Es muy probable que la compresión de fotogramas con un software como parte de una operación de captura en tiempo real tarde demasiado tiempo en realizarse.

La compresión no afecta a los fotogramas copiados en el Portapapeles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





