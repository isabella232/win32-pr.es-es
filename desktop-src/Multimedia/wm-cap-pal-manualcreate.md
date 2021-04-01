---
title: Mensaje de WM_CAP_PAL_MANUALCREATE (VFW. h)
description: El \_ mensaje MANUALCREATE Cap de WM Cap \_ \_ solicita que el controlador de captura muestre manualmente los fotogramas de vídeo y cree una nueva paleta. Puede enviar este mensaje explícitamente o mediante la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- Mensaje de WM_CAP_PAL_MANUALCREATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801868"
---
# <a name="wm_cap_pal_manualcreate-message"></a>\_ \_ Mensaje MANUALCREATE de PAL Cap de WM \_

El **mensaje \_ \_ \_ MANUALCREATE Cap de WM Cap** solicita que el controlador de captura muestre manualmente los fotogramas de vídeo y cree una nueva paleta. Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Marca de histograma de la paleta. Establezca este parámetro en **true** para cada marco incluido en la creación de la paleta óptima. Después de recopilar el último fotograma, establezca este parámetro en **false** para calcular la paleta óptima y enviarlo al controlador de captura.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de colores de la paleta. El valor máximo de este parámetro es 256. Este valor solo se usa durante la recopilación del primer fotograma de una secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

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

 

 





