---
title: WM_CAP_PAL_PASTE mensaje (Vfw.h)
description: El mensaje WM CAP PAL PASTE copia la paleta del Portapapeles \_ y la pasa a un controlador de \_ \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bedb760a444abe9b0667592855d701dc24a02b8ee57ea15ab30912a5e216d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686835"
---
# <a name="wm_cap_pal_paste-message"></a>Mensaje \_ DE PEGAR DE WM CAP \_ PAL \_

El **mensaje WM CAP PAL \_ \_ \_ PASTE** copia la paleta del Portapapeles y la pasa a un controlador de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capPalettePaste.**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste)


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**DE ERROR WM CAP SET \_ \_ \_ CALLBACK, \_**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Comentarios

Un controlador de captura usa una paleta cuando lo requiere el formato de vídeo digitalizado especificado.

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

 

 





