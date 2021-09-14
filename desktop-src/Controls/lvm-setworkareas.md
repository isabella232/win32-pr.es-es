---
title: LVM_SETWORKAREAS mensaje (Commctrl.h)
description: Establece las áreas de trabajo dentro de un control list-view. Puede enviar este mensaje explícitamente o usar la macro ListView \_ SetWorkAreas.
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
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362639"
---
# <a name="lvm_setworkareas-message"></a>Mensaje \_ SETWORKAREAS de LVM

Establece las áreas de trabajo dentro de un control list-view. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ SetWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de estructuras de la matriz en *lprc*. El número máximo de áreas de trabajo permitidas se define mediante el valor DE LV \_ MAX \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**estructuras RECT**](/previous-versions//dd162897(v=vs.85)) que contienen las nuevas áreas de trabajo del control list-view. Los valores de estas estructuras están en coordenadas de cliente. Si este parámetro es **NULL,** el área de trabajo se establecerá en el área de cliente del control. *wParam especifica* el número de estructuras de esta matriz.

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

 

