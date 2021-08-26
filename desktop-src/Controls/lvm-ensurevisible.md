---
title: LVM_ENSUREVISIBLE mensaje (Commctrl.h)
description: Garantiza que un elemento de vista de lista esté completamente visible o parcialmente, desplazando el control list-view si es necesario. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ EnsureVisible.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920305"
---
# <a name="lvm_ensurevisible-message"></a>MENSAJE \_ LVM ENSUREVISIBLE

Garantiza que un elemento de vista de lista esté completamente visible o parcialmente, desplazando el control list-view si es necesario. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ EnsureVisible.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica si el elemento debe estar completamente visible. Si este parámetro es **TRUE,** no se produce ningún desplazamiento si el elemento es al menos parcialmente visible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Se produce un error en el mensaje si el estilo de ventana [**incluye LVS \_ NOSCROLL**](list-view-window-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





