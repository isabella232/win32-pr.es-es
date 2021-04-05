---
title: Mensaje de LVM_SETITEMINDEXSTATE (commctrl. h)
description: Establece el estado de un elemento de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro SetItemIndexState de ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079131"
---
# <a name="lvm_setitemindexstate-message"></a>\_Mensaje SETITEMINDEXSTATE LVM

Establece el estado de un elemento de vista de lista. Envíe este mensaje explícitamente o mediante la [**macro \_ SetItemIndexState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para el elemento. El proceso de llamada es responsable de la asignación de esta estructura y de la configuración de los miembros.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . El proceso de llamada es responsable de la asignación de memoria para la estructura. Establezca el miembro **State** en una o varias (como una combinación bit a bit) de las marcas de [los Estados de los elementos](list-view-item-states.md) de la vista de lista. Establezca el miembro **stateMask** de la estructura para indicar los bits válidos del miembro **State** . Para obtener más información, vea el miembro **stateMask** de la estructura **LVITEM** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores de tipo **HRESULT**.



| Código devuelto                                                                                  | Descripción                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | No se pudo establecer el estado.<br/>                            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | El control de vista de lista no estaba listo para la operación.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La operación se realizó correctamente.<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





