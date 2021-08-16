---
title: TCM_INSERTITEM mensaje (Commctrl.h)
description: Inserta una nueva pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829106"
---
# <a name="tcm_insertitem-message"></a>Mensaje \_ INSERTITEM de TCM

Inserta una nueva pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la [**macro TabCtrl \_ InsertItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la nueva pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica los atributos de la pestaña. Este mensaje omite los miembros **dwState** y **dwStateMask** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la nueva pestaña si se realiza correctamente o -1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) y **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





