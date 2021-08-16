---
title: LVM_SETWORKAREAS mensaje (Commctrl.h)
description: Establece las áreas de trabajo dentro de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro SetWorkAreas de ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1060377fd9aec9014d18d206444355b052f4aafb796403e3e47fa92a0a7aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830666"
---
# <a name="lvm_setworkareas-message"></a>Mensaje \_ SETWORKAREAS de LVM

Establece las áreas de trabajo dentro de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetWorkAreas de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de estructuras de la matriz en *lprc*. El número máximo de áreas de trabajo permitidas se define mediante el valor \_ LV MAX \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**estructuras RECT**](/previous-versions//dd162897(v=vs.85)) que contienen las nuevas áreas de trabajo del control list-view. Los valores de estas estructuras están en coordenadas de cliente. Si este parámetro es **NULL,** el área de trabajo se establecerá en el área de cliente del control. *wParam* especifica el número de estructuras de esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

