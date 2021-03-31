---
title: Mensaje de WM_CAP_PAL_PASTE (VFW. h)
description: El \_ \_ \_ mensaje de pegado PAL de Cap de WM copia la paleta del portapapeles y la pasa a un controlador de captura. Puede enviar este mensaje explícitamente o mediante la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- Mensaje de WM_CAP_PAL_PASTE de Windows multimedia
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
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996191"
---
# <a name="wm_cap_pal_paste-message"></a>\_Mensaje de \_ pegado PAL de Cap de WM \_

El mensaje de **\_ \_ \_ pegado PAL de Cap de WM** copia la paleta del portapapeles y la pasa a un controlador de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Un controlador de captura usa una paleta cuando lo requiere el formato de vídeo digitalizado especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





