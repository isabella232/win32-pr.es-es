---
title: LVM_SETITEMINDEXSTATE mensaje (Commctrl.h)
description: Establece el estado de un elemento de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro SetItemIndexState de ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362695"
---
# <a name="lvm_setitemindexstate-message"></a>Mensaje \_ LVM SETITEMINDEXSTATE

Establece el estado de un elemento de vista de lista. Envíe este mensaje explícitamente o mediante la macro [**\_ SetItemIndexState de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para el elemento. El proceso de llamada es responsable de asignar esta estructura y establecer los miembros.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) El proceso de llamada es responsable de asignar memoria para la estructura . Establezca el **miembro de** estado en uno o varios (como una combinación bit a bit) de las marcas [List-View Item States.](list-view-item-states.md) Establezca el **miembro stateMask** de la estructura para indicar los bits válidos del **miembro de** estado. Para obtener más información, vea el **miembro stateMask** de la **estructura LVITEM.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores de tipo **HRESULT.**



| Código devuelto                                                                                  | Descripción                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | No se pudo establecer el estado.<br/>                            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | El control list-view no estaba listo para la operación.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | La operación se realizó correctamente.<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





