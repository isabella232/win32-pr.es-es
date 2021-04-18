---
title: Mensaje de ICM_DRAW_GETTIME (VFW. h)
description: El \_ \_ mensaje de creación de un controlador de presentación ICM solicita un controlador de representación que controla el tiempo de dibujo de los marcos para devolver el valor actual de su reloj interno. Puede enviar este mensaje explícitamente o mediante la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- Mensaje de ICM_DRAW_GETTIME de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676800"
---
# <a name="icm_draw_gettime-message"></a>\_Mensaje GETTIME de Draw ICM \_

El mensaje de **\_ creación \_** de un controlador de presentación ICM solicita un controlador de representación que controla el tiempo de dibujo de los marcos para devolver el valor actual de su reloj interno. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*
</dt> <dd>

Dirección que va a contener la hora actual. El valor devuelto debe especificarse en los ejemplos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Normalmente, este mensaje es compatible con hardware que realiza su propia descompresión asincrónica, temporización y dibujo. También se puede enviar el mensaje si el hardware se utiliza como maestro de sincronización.

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

 

 





