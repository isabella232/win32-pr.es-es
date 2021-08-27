---
title: LVM_GETNUMBEROFWORKAREAS mensaje (Commctrl.h)
description: Recupera el número de áreas de trabajo de un control list-view. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetNumberOfWorkAreas.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735dbb808755857df3dec4c5e8a021b9fe873e555607dc547bc77e67e123b948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088885"
---
# <a name="lvm_getnumberofworkareas-message"></a>Mensaje \_ GETNUMBEROFWORKAREAS de LVM

Recupera el número de áreas de trabajo de un control list-view. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetNumberOfWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor UINT que recibe el número de áreas de trabajo en el control list-view. Si se coloca cero en esta variable, no se establecen áreas de trabajo actualmente. Este valor no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 





