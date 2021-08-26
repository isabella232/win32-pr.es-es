---
title: LVM_GETGROUPINFOBYINDEX mensaje (Commctrl.h)
description: Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la macro \_ ListView GetGroupInfoByIndex.
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
ms.openlocfilehash: 482683e9d1026c1deed17bf1f05310d63ac2127a6a2a6f32b5b5d95a0fbbea3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877405"
---
# <a name="lvm_getgroupinfobyindex-message"></a>Mensaje \_ LVM GETGROUPINFOBYINDEX

Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetGroupInfoByIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del grupo.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para recibir información sobre el grupo especificado por *wParam*. El proceso de llamada es responsable de asignar memoria para la estructura y los búferes de la estructura, como el que señala el **miembro pszHeader.** Establezca los miembros de la estructura, como **cchHeader,** el tamaño del búfer al que apunta **pszHeader** en **WCHAR,** incluido el **valor NULL final.** Establezca **cbSize** en sizeof(LVGROUP).

El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





