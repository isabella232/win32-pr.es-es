---
title: LVM_GETTOPINDEX mensaje (Commctrl.h)
description: Recupera el índice del elemento visible más arriba en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetTopIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920045"
---
# <a name="lvm_gettopindex-message"></a>Mensaje \_ GETTOPINDEX de LVM

Recupera el índice del elemento visible más arriba en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetTopIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento si se realiza correctamente. Devuelve cero si el control list-view está en la vista de icono o icono pequeño, o si el control list-view está en la vista de detalles con grupos habilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





