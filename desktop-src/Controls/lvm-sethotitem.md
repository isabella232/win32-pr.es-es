---
title: LVM_SETHOTITEM mensaje (Commctrl.h)
description: Establece el elemento de acceso de acceso de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView SetHotItem.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6937cbed8150bf14eb71e167b8ed54d6f6b47ae995a3af989613cba30c7ca3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077245"
---
# <a name="lvm_sethotitem-message"></a>Mensaje \_ SETHOTITEM de LVM

Establece el elemento de acceso de acceso de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView SetHotItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que se va a establecer como elemento de acceso rápido.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento que estaba previamente en caliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





