---
title: RB_GETBARINFO mensaje (Commctrl.h)
description: Recupera información sobre el control rebar y la lista de imágenes que usa.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- RB_GETBARINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d1d1ee657f88b95b0caad254377ebca0db74b313fd7eb3fe102d4f488c14d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085095"
---
# <a name="rb_getbarinfo-message"></a>Mensaje \_ GETBARINFO de RB

Recupera información sobre el control rebar y la lista de imágenes que usa.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que recibirá la información del control rebar. Debe establecer el **miembro cbSize** de esta estructura en **sizeof**(REBARINFO) antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





