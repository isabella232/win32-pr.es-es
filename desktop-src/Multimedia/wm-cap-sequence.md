---
title: Mensaje de WM_CAP_SEQUENCE (VFW. h)
description: El mensaje de secuencia de Cap de WM \_ inicia la \_ captura de audio y vídeo de streaming a un archivo. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- Mensaje de WM_CAP_SEQUENCE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996535"
---
# <a name="wm_cap_sequence-message"></a>Mensaje de secuencia de \_ Cap de WM \_

El mensaje de **\_ \_ secuencia de Cap de WM** inicia la captura de audio y vídeo de streaming a un archivo. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Si desea modificar los parámetros que controlan la captura de streaming, use el mensaje de configuración de la secuencia de definición de Cap de WM antes de iniciar la captura. [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)

De forma predeterminada, la ventana de captura no permite que otras aplicaciones sigan ejecutándose durante la captura. Para invalidar esto, establezca el miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en **true** o instale una función de devolución de llamada yield.

Durante la captura de streaming, la ventana de captura puede emitir notificaciones de forma opcional a la aplicación de tipos específicos de condiciones. Para instalar los procedimientos de devolución de llamada para estas notificaciones, use los siguientes mensajes:

-   [**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-error.md)
-   [**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-status.md)
-   [**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**](wm-cap-set-callback-yield.md)
-   [**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-videostream.md)
-   [**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-wavestream.md)

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

 

 





