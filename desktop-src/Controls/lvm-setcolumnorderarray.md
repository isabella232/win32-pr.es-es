---
title: Mensaje de LVM_SETCOLUMNORDERARRAY (commctrl. h)
description: Establece el orden de izquierda a derecha de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetColumnOrderArray de ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078863"
---
# <a name="lvm_setcolumnorderarray-message"></a>\_Mensaje SETCOLUMNORDERARRAY LVM

Establece el orden de izquierda a derecha de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetColumnOrderArray de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en elementos, del búfer en *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz que especifica el orden en el que se deben mostrar las columnas, de izquierda a derecha. Por ejemplo, si el contenido de la matriz es {2,0,1} , el control muestra la columna 2, la columna 0 y la columna 1 en ese orden.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





