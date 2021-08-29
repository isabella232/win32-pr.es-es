---
title: WM_CAP_DLG_VIDEOFORMAT mensaje (Vfw.h)
description: El mensaje \_ WM CAP DLG VIDEOFORMAT muestra un cuadro de diálogo en el que el \_ usuario puede seleccionar el formato de \_ vídeo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaa58e99c6a07db9109a0b1a6dae25de8abd46fef2631eb539961de16455ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135404"
---
# <a name="wm_cap_dlg_videoformat-message"></a>Mensaje \_ DE \_ DLG \_ VIDEOFORMAT de WM CAP

El **mensaje WM CAP \_ \_ DLG \_ VIDEOFORMAT** muestra un cuadro de diálogo en el que el usuario puede seleccionar el formato de vídeo. El cuadro de diálogo Formato de vídeo puede usarse para seleccionar dimensiones de imagen, profundidad de bits y opciones de compresión de hardware. Puede enviar este mensaje explícitamente o mediante la [**macro capDlgVideoFormat.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat)


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Comentarios

Una vez que se devuelve este mensaje, es posible que las aplicaciones tengan que actualizar la [**estructura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) porque el usuario podría haber cambiado las dimensiones de la imagen.

El cuadro de diálogo Formato de vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo Formato de vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el **miembro fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





