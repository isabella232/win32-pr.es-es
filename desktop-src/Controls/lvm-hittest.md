---
title: Mensaje de LVM_HITTEST (commctrl. h)
description: Determina qué elemento de vista de lista, si existe, está en una posición especificada. Puede enviar este mensaje explícitamente o mediante la \_ macro HitTest de ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996907"
---
# <a name="lvm_hittest-message"></a>El \_ mensaje de LVM HITTEST

Determina qué elemento de vista de lista, si existe, está en una posición especificada. Puede enviar este mensaje explícitamente o mediante la macro [**\_ HitTest de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser 0. **Windows Vista.** Debe ser-1 si se van a recuperar los miembros **iGroup** y **iSubItem** de la estructura *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) que contiene la posición para la prueba de posicionamiento y recibe información sobre los resultados de la prueba de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento en la posición especificada, si existe, o-1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





