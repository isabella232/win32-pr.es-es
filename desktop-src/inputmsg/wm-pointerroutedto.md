---
title: Mensaje WM_POINTERROUTEDTO
description: Se envía cuando la entrada de puntero continua, para un identificador de puntero existente, realiza la transición de un proceso a otro en el contenido configurado para el encadenamiento entre procesos (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERROUTEDTO
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422189"
---
# <a name="wm_pointerroutedto-message"></a>Mensaje WM_POINTERROUTEDTO

Se envía cuando la entrada de puntero continua, para un identificador de puntero existente, realiza la transición de un proceso a otro en el contenido configurado para el encadenamiento entre procesos ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

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

Este mensaje no se envía cuando se envía un mensaje de [**WM_POINTERDOWN**](wm-pointerdown.md) para un nuevo identificador de puntero en un proceso diferente.

No se envía un mensaje de [**WM_POINTERDOWN**](wm-pointerdown.md) si se publica primero un mensaje **WM_POINTERROUTEDTO** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

