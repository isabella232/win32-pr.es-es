---
title: TCM_GETITEMRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1a8a018cf63247831e07d0b4f1a64dd1469f96dd679409480e097712bb027d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060955"
---
# <a name="tcm_getitemrect-message"></a>Mensaje \_ GETITEMRECT de TCM

Recupera el rectángulo delimitador de una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador de la pestaña, en coordenadas de ventanilla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

