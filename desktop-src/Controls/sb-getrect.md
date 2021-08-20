---
title: SB_GETRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de un elemento en una ventana de estado.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d874a5bf115918432bd6f0310a14ed026e0dc2df22da029bfca0be25649821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168741"
---
# <a name="sb_getrect-message"></a>Mensaje \_ SB GETRECT

Recupera el rectángulo delimitador de un elemento en una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento cuyo rectángulo delimitador se va a recuperar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

