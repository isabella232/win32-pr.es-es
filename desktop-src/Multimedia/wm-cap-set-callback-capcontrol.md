---
title: WM_CAP_SET_CALLBACK_CAPCONTROL mensaje (Vfw.h)
description: El mensaje CAPCONTROL de devolución de llamada DE WM CAP SET establece una función de devolución de \_ llamada en la aplicación que le da un control de grabación \_ \_ \_ preciso. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161338"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>Mensaje \_ \_ CAPCONTROL DE \_ DEVOLUCIÓN DE \_ LLAMADA DE WM CAP SET

El **mensaje \_ \_ \_ \_ CAPCONTROL de devolución de** llamada DE WM CAP SET establece una función de devolución de llamada en la aplicación que le da un control de grabación preciso. Puede enviar este mensaje explícitamente o mediante la [**macro capSetCallbackOnCapControl.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol)


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada, de tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **si** hay una captura de streaming o una sesión de captura de un solo fotograma en curso.

## <a name="remarks"></a>Observaciones

Se usa una sola función de devolución de llamada para proporcionar a la aplicación un control preciso sobre los momentos en que comienza y se completa la captura de streaming. La ventana de captura llama primero al procedimiento con *nState* establecido en CONTROLCALLBACK PREROLL después de que se hayan asignado todos los búferes y de que todas las demás preparaciones \_ de captura hayan finalizado. Esto proporciona a la aplicación la capacidad de preinselección de orígenes de vídeo, volviendo de la función de devolución de llamada en el momento exacto en que se va a iniciar la grabación. Un valor devuelto de **TRUE de** la función de devolución de llamada continúa la captura y un valor devuelto de **FALSE** anula la captura. Una vez que comience la captura, se llamará a esta función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK CAPTURING para permitir que la aplicación finalice la captura \_ devolviendo **FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





