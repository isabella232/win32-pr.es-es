---
title: LVM_SETCOLUMNORDERARRAY mensaje (Commctrl.h)
description: Establece el orden de izquierda a derecha de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro SetColumnOrderArray de ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061795"
---
# <a name="lvm_setcolumnorderarray-message"></a>Mensaje \_ SETCOLUMNORDERARRAY de LVM

Establece el orden de izquierda a derecha de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetColumnOrderArray de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en elementos, del búfer en *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz que especifica el orden en el que se deben mostrar las columnas, de izquierda a derecha. Por ejemplo, si el contenido de la matriz es , el control muestra la columna 2, la columna 0 y la {2,0,1} columna 1 en ese orden.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





