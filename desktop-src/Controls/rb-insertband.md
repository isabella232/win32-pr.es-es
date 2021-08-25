---
title: RB_INSERTBAND mensaje (Commctrl.h)
description: Inserta una nueva banda en un control rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e21020302e4dcbfeb75f4a57d37be4b5c5703668231e8ec8e9dd9bd9577cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770165"
---
# <a name="rb_insertband-message"></a>Mensaje \_ INSERTBAND de RB

Inserta una nueva banda en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la ubicación donde se insertará la banda. Si establece este parámetro en -1, el control agregará la nueva banda en la última ubicación.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define la banda que se va a insertar. Debe establecer el **miembro cbSize** de esta estructura en **sizeof**(REBARBANDINFO) antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **RB \_ INSERTBANDW** (Unicode) y **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





