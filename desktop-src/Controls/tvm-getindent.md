---
title: TVM_GETINDENT mensaje (Commctrl.h)
description: Recupera la cantidad, en píxeles, que se aplica una sangría a los elementos secundarios en relación con sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la macro \_ TreeView GetIndent.
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
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165754"
---
# <a name="tvm_getindent-message"></a>Mensaje \_ GETINDENT de TVM

Recupera la cantidad, en píxeles, que se aplica una sangría a los elementos secundarios en relación con sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView GetIndent.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de sangría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





