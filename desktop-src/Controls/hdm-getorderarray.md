---
title: HDM_GETORDERARRAY mensaje (Commctrl.h)
description: Obtiene el orden actual de izquierda a derecha de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o usar la \_ macro GetOrderArray de encabezado.
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
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061992"
---
# <a name="hdm_getorderarray-message"></a>Mensaje \_ GETORDERARRAY de HDM

Obtiene el orden actual de izquierda a derecha de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**\_ GetOrderArray de**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) encabezado.

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

## <a name="remarks"></a>Observaciones

El número de elementos *de lParam* se especifica en *wParam* y debe ser igual al número de elementos del control . Por ejemplo, el fragmento de código siguiente reservará suficiente memoria para contener los valores de índice.


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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





