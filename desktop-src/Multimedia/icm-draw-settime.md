---
title: Mensaje de ICM_DRAW_SETTIME (VFW. h)
description: El \_ \_ control SETTIME de ICM proporciona información de sincronización a un controlador de representación que controla el tiempo de dibujo de los marcos.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- Mensaje de ICM_DRAW_SETTIME de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905160"
---
# <a name="icm_draw_settime-message"></a>Desdibujado ICM \_ \_ mensaje SETTIME

El **control \_ \_ SETTIME de ICM** proporciona información de sincronización a un controlador de representación que controla el tiempo de dibujo de los marcos. La información de sincronización es el número de muestra del marco que se va a dibujar. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

Número de muestra del marco que se va a representar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Normalmente, el controlador compara el valor especificado con el número de marco asociado a la hora de su reloj interno e intenta sincronizar los dos si la diferencia es significativa.

Utilice este mensaje cuando el hardware realice su propia descompresión asincrónica, temporización y dibujo, y el hardware se base en una señal de sincronización externa (el hardware no se utiliza como maestro de sincronización).

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

 

 





