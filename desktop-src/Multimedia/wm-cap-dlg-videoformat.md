---
title: WM_CAP_DLG_VIDEOFORMAT mensaje (Vfw.h)
description: El mensaje WM CAP DLG VIDEOFORMAT muestra un cuadro de diálogo en el que \_ el usuario puede seleccionar el formato de \_ \_ vídeo.
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
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473859"
---
# <a name="wm_cap_dlg_videoformat-message"></a>Mensaje \_ DE FORMATO DE VÍDEO DE \_ DLG DE WM CAP \_

El **mensaje WM CAP \_ \_ DLG \_ VIDEOFORMAT** muestra un cuadro de diálogo en el que el usuario puede seleccionar el formato de vídeo. El cuadro de diálogo Formato de vídeo se puede usar para seleccionar las dimensiones de imagen, la profundidad de bits y las opciones de compresión de hardware. Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoFormat.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat)


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

Una vez que se devuelve este mensaje, es posible que las aplicaciones deba actualizar la [**estructura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) porque el usuario podría haber cambiado las dimensiones de la imagen.

El cuadro de diálogo Formato de vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo Formato de vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el **miembro fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





