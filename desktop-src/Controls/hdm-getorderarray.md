---
title: Mensaje de HDM_GETORDERARRAY (commctrl. h)
description: Obtiene el orden actual de izquierda a derecha de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetOrderArray.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150316"
---
# <a name="hdm_getorderarray-message"></a>HDM \_ GETORDERARRAY

Obtiene el orden actual de izquierda a derecha de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos enteros que puede contener *lParam* . Este valor debe ser igual al número de elementos del control (vea [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que reciben los valores de índice de los elementos del encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto y el búfer de *lParam* recibe el número de elemento de cada elemento del control de encabezado en el orden en el que aparecen de izquierda a derecha. De lo contrario, el mensaje devuelve cero.

## <a name="remarks"></a>Observaciones

El número de elementos de *lParam* se especifica en *wParam* y debe ser igual al número de elementos del control. Por ejemplo, el siguiente fragmento de código reservará suficiente memoria para contener los valores de índice.


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





