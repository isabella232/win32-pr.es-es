---
title: Mensaje de LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Recupera el número de áreas de trabajo en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetNumberOfWorkAreas de ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996911"
---
# <a name="lvm_getnumberofworkareas-message"></a>\_Mensaje GETNUMBEROFWORKAREAS LVM

Recupera el número de áreas de trabajo en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetNumberOfWorkAreas de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor UINT que recibe el número de áreas de trabajo en el control de vista de lista. Si se coloca cero en esta variable, no se establece ninguna área de trabajo en este momento. Este valor no puede ser **null**.

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

 

 





