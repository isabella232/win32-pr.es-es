---
title: Mensaje de LVM_FINDITEM (commctrl. h)
description: Busca un elemento de vista de lista con las características especificadas. Puede enviar este mensaje explícitamente o mediante la macro de ListView \_ FindItem.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- LVM_FINDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489077"
---
# <a name="lvm_finditem-message"></a>\_Mensaje FINDITEM LVM

Busca un elemento de vista de lista con las características especificadas. Puede enviar este mensaje explícitamente o mediante la macro de [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento en el que se va a comenzar la búsqueda o-1 para empezar desde el principio. El elemento especificado se excluye de la búsqueda.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que contiene información sobre lo que se va a buscar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento si se realiza correctamente, o-1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ FINDITEMW** (Unicode) y **\_ FINDITEMA de LVM** (ANSI)<br/>                 |



 

 





