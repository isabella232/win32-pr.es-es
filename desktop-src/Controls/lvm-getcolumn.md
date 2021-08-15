---
title: LVM_GETCOLUMN mensaje (Commctrl.h)
description: Obtiene los atributos de la columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetColumn.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65478d1d249740c630499fd4837e31d4eba7b992cf3ef3682c4e7b72d0706cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411741"
---
# <a name="lvm_getcolumn-message"></a>Mensaje \_ GETCOLUMN de LVM

Obtiene los atributos de la columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que especifica la información que se debe recuperar y recibe información sobre la columna. El **miembro mask** especifica qué atributos de columna se recuperarán. Si el miembro **mask** especifica el valor LVCF TEXT, el miembro pszText debe contener la dirección del búfer que recibe el texto del elemento y el miembro \_  **cchTextMax** debe especificar el tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





