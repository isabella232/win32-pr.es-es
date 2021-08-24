---
title: LB_INITSTORAGE mensaje (Winuser.h)
description: Asigna memoria para almacenar elementos de cuadro de lista. Este mensaje se usa antes de que una aplicación agrega un gran número de elementos a un cuadro de lista.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe873244358bf171c3fcedc994facd36e194edf38e0ee0442f12556cc4342514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544275"
---
# <a name="lb_initstorage-message"></a>Mensaje \_ LB INITSTORAGE

Asigna memoria para almacenar elementos de cuadro de lista. Este mensaje se usa antes de que una aplicación agrega un gran número de elementos a un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se agregarán.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Cantidad de memoria, en bytes, que se asignará a las cadenas de elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el número total de elementos para los que se ha asignado previamente la memoria, es decir, el número total de elementos agregados por todos los mensajes **LB \_ INITSTORAGE** correctos.

Si se produce un error en el mensaje, el valor devuelto es \_ LB ERRSPACE.

Microsoft Windows NT 4.0: este mensaje no asigna la cantidad de memoria especificada; sin embargo, siempre devuelve el valor especificado en el *parámetro wParam.*

## <a name="remarks"></a>Comentarios

El **mensaje \_ LB INITSTORAGE** ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes [**\_ LB ADDSTRING,**](lb-addstring.md) [**LB \_ INSERTSTRING,**](lb-insertstring.md) [**LB \_ DIR**](lb-dir.md)y [**LB \_ ADDFILE**](lb-addfile.md) tarden el menor tiempo posible. Puede usar estimaciones para los *parámetros wParam* *y lParam.* Si sobreestima, se asigna la memoria adicional; Si se infravalora, la asignación normal se usa para los elementos que superan la cantidad solicitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ ADDFILE**](lb-addfile.md)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ DIR**](lb-dir.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





