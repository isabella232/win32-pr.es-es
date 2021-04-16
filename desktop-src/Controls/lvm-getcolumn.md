---
title: Mensaje de LVM_GETCOLUMN (commctrl. h)
description: Obtiene los atributos de la columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro getcolumn (de ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489065"
---
# <a name="lvm_getcolumn-message"></a>\_Mensaje GETCOLUMN (LVM

Obtiene los atributos de la columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ Getcolumn (de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que especifica la información que se va a recuperar y recibe información sobre la columna. El miembro **Mask** especifica los atributos de columna que se van a recuperar. Si el miembro **Mask** especifica el \_ valor de texto LVCF, el miembro **miembros pszText** debe contener la dirección del búfer que recibe el texto del elemento y el miembro **cchTextMax** debe especificar el tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





