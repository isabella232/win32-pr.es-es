---
title: Mensaje de TVM_GETINDENT (commctrl. h)
description: Recupera la cantidad, en píxeles, a la que se aplica sangría a los elementos secundarios respecto a sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la \_ macro GetIndent de TreeView.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905583"
---
# <a name="tvm_getindent-message"></a>\_Mensaje de GETINDENT TVM

Recupera la cantidad, en píxeles, a la que se aplica sangría a los elementos secundarios respecto a sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetIndent de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





