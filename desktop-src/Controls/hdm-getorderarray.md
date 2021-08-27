---
title: HDM_GETORDERARRAY mensaje (Commctrl.h)
description: Obtiene el orden de izquierda a derecha actual de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro Header \_ GetOrderArray.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY controles de Windows mensaje
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
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062835"
---
# <a name="hdm_getorderarray-message"></a>Mensaje \_ GETORDERARRAY de HDM

Obtiene el orden de izquierda a derecha actual de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ GetOrderArray.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos enteros que *lParam* puede contener. Este valor debe ser igual al número de elementos del control [**(vea HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que reciben los valores de índice de los elementos del encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente y el búfer de *lParam* recibe el número de elemento para cada elemento del control de encabezado en el orden en que aparecen de izquierda a derecha. De lo contrario, el mensaje devuelve cero.

## <a name="remarks"></a>Comentarios

El número de elementos de *lParam* se especifica en *wParam* y debe ser igual al número de elementos del control . Por ejemplo, el siguiente fragmento de código reservará suficiente memoria para contener los valores de índice.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





