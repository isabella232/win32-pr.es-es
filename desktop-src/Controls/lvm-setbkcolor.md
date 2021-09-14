---
title: LVM_SETBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetBkColor.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061797"
---
# <a name="lvm_setbkcolor-message"></a>Mensaje \_ SETBKCOLOR de LVM

Establece el color de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Color de fondo que se establecerá o el valor \_ CLR NONE para ningún color de fondo. Los controles de vista de lista con colores de fondo se dibujan a sí mismos mucho más rápido que los que no tienen colores de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





