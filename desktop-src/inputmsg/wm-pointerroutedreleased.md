---
title: WM_POINTERROUTEDRELEASED mensaje
description: Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de AddContentWithCrossProcessChaining y que actualmente no administran la entrada de puntero) asociados a un identificador de puntero específico, cuando se recibe un mensaje WM_POINTERUP en el proceso actual.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED mensajes de entrada y notificaciones
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569492"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED mensaje

Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) y que actualmente no administran la entrada de puntero) asociados a un identificador de puntero específico, cuando se recibe un mensaje [**WM_POINTERUP**](wm-pointerup.md) en el proceso actual.


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
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

