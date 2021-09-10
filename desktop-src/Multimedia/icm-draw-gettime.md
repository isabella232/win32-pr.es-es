---
title: ICM_DRAW_GETTIME mensaje (Vfw.h)
description: El ICM DRAW GETTIME solicita un controlador de representación que controla el tiempo de dibujo de fotogramas para devolver el valor actual \_ \_ de su reloj interno. Puede enviar este mensaje explícitamente o mediante la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370549"
---
# <a name="icm_draw_gettime-message"></a>\_ICM Draw \_ GETTIME message

El **ICM \_ DRAW \_ GETTIME** solicita un controlador de representación que controla el tiempo de dibujo de fotogramas para devolver el valor actual de su reloj interno. Puede enviar este mensaje explícitamente o mediante la [**macro ICDrawGetTime.**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime)


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*
</dt> <dd>

Dirección que contiene la hora actual. El valor devuelto debe especificarse en los ejemplos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje suele ser compatible con hardware que realiza su propia descompresión asincrónica, control de tiempo y dibujo. El mensaje también se puede enviar si el hardware se usa como maestro de sincronización.

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

 

 





