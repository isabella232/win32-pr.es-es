---
title: Mensaje de LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtiene los estilos extendidos que están actualmente en uso para un control de vista de lista determinado. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetExtendedListViewStyle de ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE controles de mensajes de Windows
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
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078867"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>\_Mensaje GETEXTENDEDLISTVIEWSTYLE LVM

Obtiene los estilos extendidos que están actualmente en uso para un control de vista de lista determinado. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetExtendedListViewStyle de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que representa los estilos actualmente en uso para un determinado control de vista de lista. Este valor puede ser una combinación de [estilos de List-View extendidos](extended-list-view-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





