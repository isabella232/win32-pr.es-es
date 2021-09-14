---
title: CB_INITSTORAGE mensaje (Winuser.h)
description: Una aplicación envía el mensaje CB INITSTORAGE antes de agregar un gran número de elementos a la parte del cuadro \_ de lista de un cuadro combinado. Este mensaje asigna memoria para almacenar elementos de cuadro de lista.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174178"
---
# <a name="cb_initstorage-message"></a>Mensaje \_ CB INITSTORAGE

Una aplicación envía el mensaje **CB \_ INITSTORAGE** antes de agregar un gran número de elementos a la parte del cuadro de lista de un cuadro combinado. Este mensaje asigna memoria para almacenar elementos de cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se agregarán.

</dd> <dt>

*lParam* 
</dt> <dd>

Cantidad de memoria que se asignará para las cadenas de elemento, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje es correcto, el valor devuelto es el número total de elementos para los que se ha asignado previamente la memoria, es decir, el número total de elementos agregados por todos los mensajes **\_ INITSTORAGE** de CB correctos.

Si se produce un error en el mensaje, el valor devuelto es CB \_ ERRSPACE.

El mensaje asigna memoria y devuelve los valores correctos y de error descritos anteriormente.

## <a name="remarks"></a>Observaciones

El **mensaje CB \_ INITSTORAGE** ayuda a acelerar la inicialización de cuadros combinados que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los siguientes mensajes [**\_ CB ADDSTRING,**](cb-addstring.md) [**CB \_ INSERTSTRING**](cb-insertstring.md)y [**CB \_ DIR**](cb-dir.md) tarden el menor tiempo posible. Puede usar estimaciones para los *parámetros wParam* *y lParam.* Si sobreestima, se asigna la memoria adicional; si se subvalora, se usa la asignación normal para los elementos que superan la cantidad solicitada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





