---
title: Mensaje de TVM_SORTCHILDRENCB (commctrl. h)
description: Ordena los elementos de la vista de árbol usando una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la \_ macro SortChildrenCB de TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492838"
---
# <a name="tvm_sortchildrencb-message"></a>\_Mensaje de SORTCHILDRENCB TVM

Ordena los elementos de la vista de árbol usando una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortChildrenCB de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) . El miembro **lpfnCompare** es la dirección de la función de devolución de llamada definida por la aplicación, a la que se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista. Para obtener más información sobre la función de devolución de llamada, vea la descripción de **TVSORTCB**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





