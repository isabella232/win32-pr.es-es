---
title: Mensaje de ICM_DRAW_START_PLAY (VFW. h)
description: El \_ \_ \_ mensaje de reproducción para el inicio de Draw ICM proporciona las horas de inicio y finalización de una operación de reproducción a un controlador de representación. Puede enviar este mensaje explícitamente o mediante la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- Mensaje de ICM_DRAW_START_PLAY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150178"
---
# <a name="icm_draw_start_play-message"></a>Reinicio de la \_ reproducción del dibujo ICM \_ \_

El mensaje de reproducción para el **\_ Inicio de Draw \_ \_ ICM** proporciona las horas de inicio y finalización de una operación de reproducción a un controlador de representación. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*
</dt> <dd>

Hora de inicio.

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*Cartuchos*
</dt> <dd>

Hora de finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje precede a los datos de fotogramas enviados al controlador de representación.

Las unidades de *lFrom* y *lTo* se especifican con el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) . En el caso de los datos de vídeo, suele ser un número de marco. Para obtener más información sobre la velocidad de reproducción, vea los miembros **dwRate** y **dwScale** de la estructura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .

Si la hora de finalización es menor que la hora de inicio, se invierte la dirección de reproducción.

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

 

 





