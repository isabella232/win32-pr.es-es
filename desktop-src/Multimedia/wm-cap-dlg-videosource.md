---
title: WM_CAP_DLG_VIDEOSOURCE mensaje (Vfw.h)
description: El mensaje DLG VIDEOSOURCE de WM CAP muestra un cuadro de diálogo en el que \_ el usuario puede controlar el origen del \_ \_ vídeo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f05d7e3dc421759229adffa4ecc4b78affc26f1b4244887b017614c2ab4d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803885"
---
# <a name="wm_cap_dlg_videosource-message"></a>Mensaje \_ DE \_ DLG \_ VIDEOSOURCE DE WM CAP

El **mensaje \_ \_ DLG \_ VIDEOSOURCE** de WM CAP muestra un cuadro de diálogo en el que el usuario puede controlar el origen del vídeo. El cuadro de diálogo Origen de vídeo puede contener controles que seleccionan orígenes de entrada; modificar el matiz, el contraste, el brillo de la imagen; y modifican la calidad del vídeo antes de digitalizar las imágenes en el búfer de fotogramas. Puede enviar este mensaje explícitamente o mediante la [**macro capDlgVideoSource.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource)


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Comentarios

El cuadro de diálogo Origen de vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo Origen de vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el **miembro fHasDlgVideoSource** de la [**estructura CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)

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

 

 





