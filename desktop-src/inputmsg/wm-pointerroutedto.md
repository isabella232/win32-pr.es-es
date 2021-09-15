---
title: WM_POINTERROUTEDTO mensaje
description: Se envía cuando la entrada de puntero en curso, para un identificador de puntero existente, pasa de un proceso a otro a través del contenido configurado para el encadenamiento entre procesos (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569485"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO mensaje

Se envía cuando la entrada de puntero en curso, para un identificador de puntero existente, pasa de un proceso a otro a través del contenido configurado para el encadenamiento entre procesos ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Este mensaje se envía al proceso que no recibe actualmente la entrada de puntero.


```C++
#define WM_POINTERROUTEDTO       0x0251
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

Este mensaje no se envía cuando se [**publica WM_POINTERDOWN**](wm-pointerdown.md) mensaje para un nuevo identificador de puntero en un proceso diferente.

No [**WM_POINTERDOWN**](wm-pointerdown.md) se envía un mensaje de WM_POINTERROUTEDTO **se** publica primero.

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

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

