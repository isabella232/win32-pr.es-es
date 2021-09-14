---
title: ICM_DRAW_WINDOW mensaje (Vfw.h)
description: El ICM draw window notifica a un controlador de representación que la ventana especificada para ICM el mensaje DRAW BEGIN debe volver a \_ \_ \_ \_ dibujarse.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246309"
---
# <a name="icm_draw_window-message"></a>\_ICM Mensaje \_ DRAW WINDOW

El **ICM \_ DRAW \_ WINDOW** notifica a un controlador de representación que la ventana especificada para ICM el mensaje [**DRAW \_ \_ BEGIN**](icm-draw-begin.md) debe volver a dibujarse. La ventana se ha movido o se ha ocultado temporalmente. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawWindow.**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow)


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Prc*
</dt> <dd>

Puntero al rectángulo de destino en coordenadas de pantalla. Si este parámetro apunta a un rectángulo vacío, se debe desactivar el dibujo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje es compatible con hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo.

Los controladores de superposición de vídeo usan este mensaje para dibujar cuando la ventana se oculta o se mueve. Cuando otras ventanas ocultan completamente una ventana ICM [**\_ para DRAW \_ BEGIN,**](icm-draw-begin.md) el rectángulo de destino está vacío. Los controladores deben desactivar el hardware de superposición de vídeo cuando se produce esta condición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





