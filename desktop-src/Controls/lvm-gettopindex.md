---
title: Mensaje de LVM_GETTOPINDEX (commctrl. h)
description: Recupera el índice del elemento visible más alto cuando está en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la \_ macro GetTopIndex de ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX controles de mensajes de Windows
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
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658335"
---
# <a name="lvm_gettopindex-message"></a>\_Mensaje GETTOPINDEX LVM

Recupera el índice del elemento visible más alto cuando está en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetTopIndex de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento si se realiza correctamente. Devuelve cero si el control de vista de lista está en la vista de icono o de iconos pequeños, o si el control de vista de lista está en la vista de detalles con los grupos habilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





