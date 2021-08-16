---
title: LVM_GETEXTENDEDLISTVIEWSTYLE mensaje (Commctrl.h)
description: Obtiene los estilos extendidos que están actualmente en uso para un control de vista de lista determinado. Puede enviar este mensaje explícitamente o usar la \_ macro GetExtendedListViewStyle de ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04b2f83f5a8bd55f01aa84e315512c5ccb1b28b17f196c0199fc417544a6737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968305"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>Mensaje DE LVM \_ GETEXTENDEDLISTVIEWSTYLE

Obtiene los estilos extendidos que están actualmente en uso para un control de vista de lista determinado. Puede enviar este mensaje explícitamente o usar la macro [**\_ GetExtendedListViewStyle de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **DWORD que** representa los estilos actualmente en uso para un control de vista de lista determinado. Este valor puede ser una combinación de [estilos de List-View extendidos.](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





