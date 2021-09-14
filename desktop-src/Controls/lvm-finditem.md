---
title: LVM_FINDITEM mensaje (Commctrl.h)
description: Busca un elemento de vista de lista con las características especificadas. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ FindItem.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- LVM_FINDITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061857"
---
# <a name="lvm_finditem-message"></a>Mensaje \_ FINDITEM de LVM

Busca un elemento de vista de lista con las características especificadas. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ FindItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento con el que se iniciará la búsqueda o -1 para comenzar desde el principio. El elemento especificado se excluye de la búsqueda.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que contiene información sobre lo que se va a buscar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento si se realiza correctamente o -1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ FINDITEMW** (Unicode) y **LVM \_ FINDITEMA** (ANSI)<br/>                 |



 

 





