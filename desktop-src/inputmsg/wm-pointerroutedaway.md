---
title: WM_POINTERROUTEDAWAY mensaje
description: Se produce en el proceso que recibe la entrada cuando la entrada del puntero se enruta a otro proceso. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569493"
---
# <a name="wm_pointerroutedaway-message"></a>WM_POINTERROUTEDAWAY mensaje

Se produce en el proceso que recibe la entrada cuando la entrada del puntero se enruta a otro proceso.

Se envía cuando la entrada de puntero pasa de un proceso a otro a través del contenido configurado para el encadenamiento entre procesos ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Este mensaje se envía al proceso que recibe actualmente la entrada de puntero.


```C++
#define WM_POINTERROUTEDAWAY       0x0252
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

## <a name="remarks"></a>Observaciones

Este mensaje no se envía con un mensaje [**WM_POINTERUP**](wm-pointerup.md) o un [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 

