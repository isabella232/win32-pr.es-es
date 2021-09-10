---
title: WM_CAP_PAL_MANUALCREATE mensaje (Vfw.h)
description: El mensaje WM CAP PAL MANUALCREATE solicita que el controlador de captura muestree manualmente fotogramas de vídeo \_ y cree una nueva \_ \_ paleta. Puede enviar este mensaje explícitamente o mediante la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371468"
---
# <a name="wm_cap_pal_manualcreate-message"></a>WM \_ CAP \_ PAL \_ MANUALCREATE message

El **mensaje WM CAP PAL \_ \_ \_ MANUALCREATE** solicita que el controlador de captura muestree manualmente fotogramas de vídeo y cree una nueva paleta. Puede enviar este mensaje explícitamente o mediante la [**macro capPaletteManual.**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual)


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Marca de histograma de paleta. Establezca este parámetro en **TRUE para** cada fotograma incluido en la creación de la paleta óptima. Una vez recopilado el último fotograma, establezca este parámetro en **FALSE** para calcular la paleta óptima y enviarlo al controlador de captura.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de colores de la paleta. El valor máximo de este parámetro es 256. Este valor solo se usa durante la recopilación del primer fotograma de una secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

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

 

 





