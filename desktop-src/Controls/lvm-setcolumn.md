---
title: Mensaje de LVM_SETCOLUMN (commctrl. h)
description: Establece los atributos de una columna de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetColumn de ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN controles de mensajes de Windows
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
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996428"
---
# <a name="lvm_setcolumn-message"></a>\_Mensaje SETCOLUMN LVM

Establece los atributos de una columna de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contiene los nuevos atributos de columna. El miembro **Mask** especifica los atributos de columna que se van a establecer. Si el miembro **Mask** especifica el \_ valor de texto LVCF, el miembro **miembros pszText** es la dirección de una cadena terminada en NULL y se omite el miembro **cchTextMax** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) y **\_ SETCOLUMNW de LVM** (ANSI)<br/>               |



 

 





