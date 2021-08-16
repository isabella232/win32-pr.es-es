---
title: WM_CAP_SET_CALLBACK_FRAME mensaje (Vfw.h)
description: El mensaje WM CAP SET CALLBACK FRAME establece una función de devolución \_ de llamada de versión preliminar en la \_ \_ \_ aplicación. AVICap llama a este procedimiento cuando la ventana de captura captura fotogramas de vista previa. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85321483639135db31750cacf76cc5f0dc4ad42e96474efa1dc17ac84ba4a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369513"
---
# <a name="wm_cap_set_callback_frame-message"></a>Mensaje WM \_ CAP \_ SET \_ CALLBACK \_ FRAME

El **mensaje WM CAP SET \_ \_ \_ CALLBACK \_ FRAME** establece una función de devolución de llamada de versión preliminar en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura captura fotogramas de vista previa. Puede enviar este mensaje explícitamente o mediante la [**macro capSetCallbackOnFrame.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe)


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de vista previa, de [**tipo capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **si** la captura de streaming o una sesión de captura de un solo fotograma están en curso.

## <a name="remarks"></a>Comentarios

La ventana de captura llama a la función de devolución de llamada antes de mostrar fotogramas de vista previa. Esto permite que una aplicación modifique el marco si lo desea. Esta función de devolución de llamada no se usa durante la captura de vídeo de streaming.

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

 

 





