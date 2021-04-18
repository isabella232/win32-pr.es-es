---
title: Mensaje de WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: El \_ \_ \_ mensaje CAPCONTROL de devolución de llamada del conjunto de Cap \_ de WM establece una función de devolución de llamada en la aplicación, lo que le otorga un control de grabación preciso. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_CAPCONTROL de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666027"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>\_Mensaje de \_ \_ CAPCONTROL de devolución de llamada de límite de Cap de WM \_

El **mensaje \_ CAPCONTROL de \_ devolución de \_ llamada \_ del conjunto de Cap de WM** establece una función de devolución de llamada en la aplicación, lo que le otorga un control de grabación preciso. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada, de tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si una captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

Se utiliza una función de devolución de llamada única para proporcionar a la aplicación un control preciso sobre los momentos en que se inicia y finaliza la captura de streaming. En primer lugar, la ventana de captura llama al procedimiento con *nState* establecido en CONTROLCALLBACK \_ preroll una vez que se han asignado todos los búferes y se han completado todos los demás preparados de captura. Esto proporciona a la aplicación la capacidad de revertir los orígenes de vídeo y volver de la función de devolución de llamada en el momento en que se inicia la grabación. Un valor devuelto de **true** desde la función de devolución de llamada continúa la captura y un valor devuelto de **false** anula la captura. Una vez iniciada la captura, se llama a esta función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK \_ para permitir que la aplicación finalice la captura devolviendo **false**.

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

 

 





