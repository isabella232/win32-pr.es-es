---
title: WM_CAP_DLG_VIDEODISPLAY mensaje (Vfw.h)
description: El mensaje DLG VIDEODISPLAY de WM CAP muestra un cuadro de diálogo en el que el usuario \_ puede establecer o ajustar la salida del \_ \_ vídeo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473860"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>Mensaje \_ DE \_ VIDEODISPLAY DE DLG \_ DE WM CAP

El **mensaje \_ \_ DLG \_ VIDEODISPLAY** de WM CAP muestra un cuadro de diálogo en el que el usuario puede establecer o ajustar la salida del vídeo. Este cuadro de diálogo puede contener controles que afectan al matiz, el contraste y el brillo de la imagen mostrada, así como la alineación del color de la clave. Puede enviar este mensaje explícitamente o mediante la [**macro capDlgVideoDisplay.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay)


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

Los controles de este cuadro de diálogo no afectan a los datos de vídeo digitalizados; afectan solo a la salida o a la presentación de la señal de vídeo.

El cuadro de diálogo Presentación de vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo De visualización de vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el **miembro fHasDlgVideoDisplay** de la [**estructura CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)

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

 

 





