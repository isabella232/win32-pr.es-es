---
title: LVM_SETCOLUMN mensaje (Commctrl.h)
description: Establece los atributos de una columna de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ SetColumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca00e62d941a753c70e0dd31c1af4003fe639d49503be7009fe5a010febf0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019223"
---
# <a name="lvm_setcolumn-message"></a>Mensaje \_ SETCOLUMN de LVM

Establece los atributos de una columna de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contiene los nuevos atributos de columna. El **miembro mask** especifica qué atributos de columna se establecerán. Si el **miembro mask** especifica el valor LVCF TEXT, el miembro pszText es la dirección de una cadena terminada en NULL y el miembro \_ **cchTextMax** se omite. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) y **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





