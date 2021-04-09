---
title: Mensaje de LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupInfoByIndex de ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150545"
---
# <a name="lvm_getgroupinfobyindex-message"></a>\_Mensaje GETGROUPINFOBYINDEX LVM

Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la [**macro \_ GetGroupInfoByIndex de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice del grupo.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para recibir información sobre el grupo especificado por *wParam*. El proceso de llamada es responsable de la asignación de memoria para la estructura y los búferes de la estructura, como el que señala el miembro **pszHeader** . Establezca los miembros contingentes de la estructura, como **cchHeader** el tamaño del búfer al que apunta **pszHeader** en **WCHARs** , incluido el **valor null** final. Establezca **cbSize** en SIZEOF (LVGROUP).

El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





