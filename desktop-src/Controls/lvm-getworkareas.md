---
title: LVM_GETWORKAREAS mensaje (Commctrl.h)
description: Recupera las áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetWorkAreas.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aed6173ef00860900d7690199cfb2c81535f088790290e30cc01898666bb068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968235"
---
# <a name="lvm_getworkareas-message"></a>Mensaje \_ GETWORKAREAS de LVM

Recupera las áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de estructuras [**RECT**](/previous-versions//dd162897(v=vs.85)) de la matriz en *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**estructuras RECT**](/previous-versions//dd162897(v=vs.85)) que reciben las áreas de trabajo actuales del control list-view. Los valores de estas estructuras están en coordenadas de cliente. *wParam* especifica el número de estructuras de esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

