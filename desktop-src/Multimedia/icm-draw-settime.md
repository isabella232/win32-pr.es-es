---
title: ICM_DRAW_SETTIME mensaje (Vfw.h)
description: El ICM DRAW SETTIME proporciona información de sincronización a un controlador de representación que \_ controla el tiempo de dibujo de \_ fotogramas.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME mensaje Windows Multimedia
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
ms.openlocfilehash: 62c291b736b0138386c235703c29fffdae470d011f55284e8aaac4c4cfd604a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691145"
---
# <a name="icm_draw_settime-message"></a>\_ICM Draw \_ SETTIME message

El **ICM \_ DRAW \_ SETTIME proporciona** información de sincronización a un controlador de representación que controla el tiempo de dibujo de fotogramas. La información de sincronización es el número de ejemplo del marco que se va a dibujar. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawSetTime.**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime)


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

Número de ejemplo del marco que se representará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Normalmente, el controlador compara el valor especificado con el número de fotograma asociado a la hora de su reloj interno e intenta sincronizar los dos si la diferencia es significativa.

Use este mensaje cuando el hardware realice su propia descompresión asincrónica, tiempo y dibujo, y el hardware se base en una señal de sincronización externa (el hardware no se usa como maestro de sincronización).

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

 

 





