---
title: LVM_GETHOTCURSOR mensaje (Commctrl.h)
description: Recupera el valor HCURSOR usado cuando el puntero está sobre un elemento mientras está habilitado el seguimiento en caliente. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetHotCursor.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540805"
---
# <a name="lvm_gethotcursor-message"></a>Mensaje \_ GETHOTCURSOR de LVM

Recupera el valor HCURSOR usado cuando el puntero está sobre un elemento mientras está habilitado el seguimiento en caliente. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetHotCursor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HCURSOR que es el identificador del cursor que usa el control de vista de lista cuando está habilitado el seguimiento en caliente.

## <a name="remarks"></a>Comentarios

Un control de vista de lista usa el seguimiento en caliente y la selección del mouse cuando se establece el estilo [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





