---
title: Mensaje de LVM_GETWORKAREAS (commctrl. h)
description: Recupera las áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetWorkAreas de ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492395"
---
# <a name="lvm_getworkareas-message"></a>\_Mensaje GETWORKAREAS LVM

Recupera las áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetWorkAreas de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El número de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) de la matriz en *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) que reciben las áreas de trabajo actuales del control de vista de lista. Los valores de estas estructuras se encuentran en coordenadas de cliente. *wParam* especifica el número de estructuras de esta matriz.

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

 

