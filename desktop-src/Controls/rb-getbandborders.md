---
title: RB_GETBANDBORDERS mensaje (Commctrl.h)
description: Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6b07303c10ef6f466907b11cf0e100927f63480690e77ac3dcbe80df80af97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409717"
---
# <a name="rb_getbandborders-message"></a>Mensaje \_ GETBANDBORDERS de RB

Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda para la que se recuperarán los bordes.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibirá los bordes de banda. Si el control rebar tiene el estilo [**\_ BANDBORDERS de RBS,**](rebar-control-styles.md) cada miembro de esta estructura recibirá el número de píxeles, en el lado correspondiente de la banda, que constituyen el borde. Si el control rebar no tiene el estilo **\_ BANDBORDERS de RBS,** solo el miembro izquierdo de esta estructura recibe información válida. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

