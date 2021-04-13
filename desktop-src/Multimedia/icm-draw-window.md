---
title: Mensaje de ICM_DRAW_WINDOW (VFW. h)
description: El mensaje de la \_ \_ ventana de dibujo ICM notifica a un controlador de representación que la ventana especificada para el mensaje de inicio de Draw de ICM \_ \_ debe volver a dibujarse.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- Mensaje de ICM_DRAW_WINDOW de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490133"
---
# <a name="icm_draw_window-message"></a>Mensaje de ventana de \_ dibujo ICM \_

El mensaje de la **\_ \_ ventana de dibujo ICM** notifica a un controlador de representación que la ventana especificada para el mensaje de [**Inicio de \_ Draw \_ de ICM**](icm-draw-begin.md) debe volver a dibujarse. La ventana se ha cambiado o se ha ocultado temporalmente. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Puntero al rectángulo de destino en coordenadas de pantalla. Si este parámetro señala a un rectángulo vacío, el dibujo debe estar desactivado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje es compatible con hardware que realiza su propia descompresión, temporización y dibujo asincrónicos.

Los controladores de superposición de vídeo usan este mensaje para dibujar cuando la ventana se oculta o se mueve. Cuando una ventana especificada para [**el \_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) está totalmente oculta en otras ventanas, el rectángulo de destino está vacío. Los controladores deben desactivar el hardware de superposición de vídeo cuando se produce esta condición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





