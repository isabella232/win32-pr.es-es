---
title: TVM_SORTCHILDRENCB mensaje (Commctrl.h)
description: Ordena los elementos de vista de árbol mediante una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la macro \_ TreeView SortChildrenCB.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165601"
---
# <a name="tvm_sortchildrencb-message"></a>Mensaje \_ DE TVM SORTCHILDRENCB

Ordena los elementos de vista de árbol mediante una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView SortChildrenCB.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TVSORTCB.**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) El **miembro lpfnCompare** es la dirección de la función de devolución de llamada definida por la aplicación, a la que se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista. Para obtener más información sobre la función de devolución de llamada, vea la descripción de **TVSORTCB**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





