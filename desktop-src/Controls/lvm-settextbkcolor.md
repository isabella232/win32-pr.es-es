---
title: LVM_SETTEXTBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetTextBkColor.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362658"
---
# <a name="lvm_settextbkcolor-message"></a>Mensaje \_ SETTEXTBKCOLOR de LVM

Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SetTextBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo color de fondo de texto. Puede ser CLR \_ NONE para ningún color de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





