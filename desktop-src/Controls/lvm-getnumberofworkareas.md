---
title: LVM_GETNUMBEROFWORKAREAS mensaje (Commctrl.h)
description: Recupera el número de áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetNumberOfWorkAreas.
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
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061821"
---
# <a name="lvm_getnumberofworkareas-message"></a>Mensaje \_ GETNUMBEROFWORKAREAS de LVM

Recupera el número de áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetNumberOfWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor UINT que recibe el número de áreas de trabajo del control de vista de lista. Si se coloca cero en esta variable, no se establece actualmente ninguna área de trabajo. Este valor no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 





