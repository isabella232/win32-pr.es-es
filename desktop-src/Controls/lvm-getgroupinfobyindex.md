---
title: LVM_GETGROUPINFOBYINDEX mensaje (Commctrl.h)
description: Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupInfoByIndex de ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974089"
---
# <a name="lvm_getgroupinfobyindex-message"></a>Mensaje \_ LVM GETGROUPINFOBYINDEX

Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la macro [**\_ GetGroupInfoByIndex de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del grupo.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para recibir información sobre el grupo especificado por *wParam*. El proceso de llamada es responsable de asignar memoria para la estructura y los búferes de la estructura, como el que señala el **miembro pszHeader.** Establezca los miembros eventuales de la estructura, como **cchHeader,** el tamaño del búfer al que apunta **pszHeader** en **WCHARs,** incluido el **valor NULL final.** Establezca **cbSize** en sizeof(LVGROUP).

El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





