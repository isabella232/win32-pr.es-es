---
title: Mensaje WM_POINTERROUTEDRELEASED
description: Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de AddContentWithCrossProcessChaining y no que actualmente controla la entrada de puntero) que se asocian a un identificador de puntero específico, cuando se recibe un mensaje de WM_POINTERUP en el proceso actual.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERROUTEDRELEASED
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422326"
---
# <a name="wm_pointerroutedreleased-message"></a>Mensaje WM_POINTERROUTEDRELEASED

Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) y no que actualmente controla la entrada de puntero) que se asocian a un identificador de puntero específico, cuando se recibe un mensaje de [**WM_POINTERUP**](wm-pointerup.md) en el proceso actual.


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sin usar.

</dd> <dt>

*lParam* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

NULL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

