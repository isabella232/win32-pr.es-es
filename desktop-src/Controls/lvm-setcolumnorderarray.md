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
ms.openlocfilehash: 9931a7d2c12da02f928c21727292d7d1ce4a430790660afb99ede4bf717c38c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077305"
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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





