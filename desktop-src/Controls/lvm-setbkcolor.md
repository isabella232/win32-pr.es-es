---
title: Mensaje de LVM_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetBkColor de ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996644"
---
# <a name="lvm_setbkcolor-message"></a>\_Mensaje SETBKCOLOR LVM

Establece el color de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetBkColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Color de fondo que se va a establecer o el \_ valor NONE de CLR para ningún color de fondo. Los controles de vista de lista con colores de fondo se vuelven a dibujar con mayor rapidez que los que no tienen colores de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





