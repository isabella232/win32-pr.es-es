---
title: LVM_GETCOLUMNORDERARRAY mensaje (Commctrl.h)
description: Obtiene el orden de las columnas de izquierda a derecha actual en un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetColumnOrderArray.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061855"
---
# <a name="lvm_getcolumnorderarray-message"></a>Mensaje \_ GETCOLUMNORDERARRAY de LVM

Obtiene el orden de las columnas de izquierda a derecha actual en un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetColumnOrderArray.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de columnas del control list-view.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que recibe los valores de índice de las columnas del control list-view. La matriz debe ser lo suficientemente grande como para contener *elementos wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve un valor distinto de cero y el búfer de *lParam* recibe el índice de columna de cada columna del control en el orden en que aparecen de izquierda a derecha. De lo contrario, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





