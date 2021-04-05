---
title: Mensaje de LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtiene el orden de izquierda a derecha actual de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetColumnOrderArray de ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078871"
---
# <a name="lvm_getcolumnorderarray-message"></a>\_Mensaje GETCOLUMNORDERARRAY LVM

Obtiene el orden de izquierda a derecha actual de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetColumnOrderArray de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El número de columnas en el control de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que recibe los valores de índice de las columnas en el control de vista de lista. La matriz debe ser lo suficientemente grande como para contener los elementos *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, devuelve un valor distinto de cero y el búfer de *lParam* recibe el índice de columna de cada columna del control en el orden en que aparecen de izquierda a derecha. De lo contrario, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





