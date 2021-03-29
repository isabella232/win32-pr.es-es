---
title: Mensaje de WM_CAP_PAL_AUTOCREATE (VFW. h)
description: El \_ mensaje de creación automática de Cap de WM Cap \_ \_ solicita que el vídeo de ejemplo del controlador de captura muestre fotogramas y cree automáticamente una nueva paleta. Puede enviar este mensaje explícitamente o mediante la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- Mensaje de WM_CAP_PAL_AUTOCREATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665957"
---
# <a name="wm_cap_pal_autocreate-message"></a>Mensaje de creación de la \_ PAL de Cap de WM \_ \_

El mensaje de creación automática de **Cap de WM \_ Cap \_ \_** solicita que el vídeo de ejemplo del controlador de captura muestre fotogramas y cree automáticamente una nueva paleta. Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Número de fotogramas que se van a muestrear.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de colores de la paleta. El valor máximo de este parámetro es 256.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

La secuencia de vídeo muestreada debe incluir todos los colores que desee en la paleta. Para obtener la mejor paleta, puede que tenga que mostrar la secuencia completa en lugar de una parte de ella.

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

 

 





