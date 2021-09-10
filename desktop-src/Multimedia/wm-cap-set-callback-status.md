---
title: WM_CAP_SET_CALLBACK_STATUS mensaje (Vfw.h)
description: El mensaje WM \_ CAP \_ SET \_ CALLBACK STATUS establece una función de \_ devolución de llamada de estado en la aplicación. AVICap llama a este procedimiento cada vez que cambia el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371491"
---
# <a name="wm_cap_set_callback_status-message"></a>Mensaje DE \_ ESTADO DE \_ \_ DEVOLUCIÓN DE LLAMADA \_ DE WM CAP SET

El **mensaje WM CAP SET \_ \_ \_ CALLBACK \_ STATUS** establece una función de devolución de llamada de estado en la aplicación. AVICap llama a este procedimiento cada vez que cambia el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capSetCallbackOnStatus.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus)


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de estado, de tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada de estado instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **si** la captura de streaming o una sesión de captura de un solo fotograma están en curso.

## <a name="remarks"></a>Observaciones

Opcionalmente, las aplicaciones pueden establecer una función de devolución de llamada de estado. Si se establece, AVICap llama a este procedimiento en las situaciones siguientes:

-   Se ha completado una sesión de captura.
-   Un controlador de captura conectado correctamente a una ventana de captura.
-   Se crea una paleta óptima.
-   Se notifica el número de fotogramas capturados.

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

 

 





