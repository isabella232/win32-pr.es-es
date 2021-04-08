---
title: Mensaje de LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcula el número de elementos que pueden ajustarse verticalmente en el área visible de un control de vista de lista cuando está en la vista de lista o de informe. Solo se cuentan los elementos totalmente visibles. Puede enviar este mensaje explícitamente o mediante la \_ macro GetCountPerPage de ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078870"
---
# <a name="lvm_getcountperpage-message"></a>\_Mensaje GETCOUNTPERPAGE LVM

Calcula el número de elementos que pueden ajustarse verticalmente en el área visible de un control de vista de lista cuando está en la vista de lista o de informe. Solo se cuentan los elementos totalmente visibles. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetCountPerPage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos totalmente visibles si se realiza correctamente. Si la vista actual es un icono o una vista de iconos pequeños, el valor devuelto es el número total de elementos del control de vista de lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





