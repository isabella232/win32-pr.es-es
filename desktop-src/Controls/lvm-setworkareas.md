---
title: Mensaje de LVM_SETWORKAREAS (commctrl. h)
description: Establece las áreas de trabajo dentro de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetWorkAreas de ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996903"
---
# <a name="lvm_setworkareas-message"></a>\_Mensaje SETWORKAREAS LVM

Establece las áreas de trabajo dentro de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetWorkAreas de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El número de estructuras de la matriz en *LPRC*. El número máximo de áreas de trabajo permitido se define mediante el \_ valor de LV Max \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) que contienen las nuevas áreas de trabajo del control de vista de lista. Los valores de estas estructuras se encuentran en coordenadas de cliente. Si este parámetro es **null**, el área de trabajo se establecerá en el área cliente del control. *wParam* especifica el número de estructuras de esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar controles List-View](using-list-view-controls.md)
</dt> </dl>

 

