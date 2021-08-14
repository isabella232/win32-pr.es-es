---
title: LVM_GETCOLUMNWIDTH mensaje (Commctrl.h)
description: Obtiene el ancho de una columna en la vista de informe o lista. Puede enviar este mensaje explícitamente o mediante la \_ macro ListView GetColumnWidth.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800ab7172ec489b84506cc55a342325527f38e447fc2bae635c2e5688a142b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411511"
---
# <a name="lvm_getcolumnwidth-message"></a>Mensaje \_ GETCOLUMNWIDTH de LVM

Obtiene el ancho de una columna en la vista de informe o lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetColumnWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna. Este parámetro se omite en la vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de columna si se realiza correctamente o cero en caso contrario. Si este mensaje se envía a un control de vista de lista con el estilo [**LVS \_ REPORT**](list-view-window-styles.md) y la columna especificada no existe, el valor devuelto no está definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





