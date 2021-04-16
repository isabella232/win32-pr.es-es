---
title: Mensaje de WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: El \_ mensaje del \_ marco de \_ devolución de llamada del conjunto de Cap de WM \_ establece una función de devolución de llamada de vista previa en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura captura los fotogramas de vista previa. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_FRAME de Windows multimedia
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
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676793"
---
# <a name="wm_cap_set_callback_frame-message"></a>\_Mensaje de \_ marco de devolución de llamada del conjunto de Cap de WM \_ \_

El mensaje del **\_ marco de devolución de \_ \_ llamada \_ del conjunto de Cap de WM** establece una función de devolución de llamada de vista previa en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura captura los fotogramas de vista previa. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de vista previa, de tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

La ventana captura llama a la función de devolución de llamada antes de mostrar los marcos de vista previa. Esto permite que una aplicación modifique el marco si se desea. Esta función de devolución de llamada no se utiliza durante la captura de vídeo de streaming.

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

 

 





