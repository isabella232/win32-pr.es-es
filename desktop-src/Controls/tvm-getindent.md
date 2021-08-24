---
title: TVM_GETINDENT mensaje (Commctrl.h)
description: Recupera la cantidad, en píxeles, que se aplica sangría a los elementos secundarios en relación con sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetIndent.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee65da49efc19954209b2694d783761017d8c2ae53030e755b8bea61213276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834185"
---
# <a name="tvm_getindent-message"></a>Mensaje \_ GETINDENT de TVM

Recupera la cantidad, en píxeles, que se aplica sangría a los elementos secundarios en relación con sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetIndent.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de sangría.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





