---
title: Mensaje de WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: El \_ \_ \_ \_ mensaje de estado de devolución de llamada de límite de Cap de WM establece una función de devolución de llamada de estado en la aplicación. AVICap llama a este procedimiento cada vez que cambia el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_STATUS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489383"
---
# <a name="wm_cap_set_callback_status-message"></a>\_Mensaje de \_ \_ Estado de devolución de llamada de límite de Cap de WM \_

El mensaje de **\_ Estado de devolución de \_ \_ llamada \_ de límite de Cap de WM** establece una función de devolución de llamada de estado en la aplicación. AVICap llama a este procedimiento cada vez que cambia el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de estado, de tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de estado instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer opcionalmente una función de devolución de llamada de estado. Si se establece, AVICap llama a este procedimiento en las siguientes situaciones:

-   Se ha completado una sesión de captura.
-   Un controlador de captura se conectó correctamente a una ventana de captura.
-   Se crea una paleta óptima.
-   Se registra el número de fotogramas capturados.

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

 

 





