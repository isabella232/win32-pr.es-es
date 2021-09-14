---
title: LB_GETSELITEMS mensaje (Winuser.h)
description: Rellena un búfer con una matriz de enteros que especifican los números de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061878"
---
# <a name="lb_getselitems-message"></a>Mensaje \_ LB GETSELITEMS

Rellena un búfer con una matriz de enteros que especifican los números de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de elementos seleccionados cuyos números de elemento se van a colocar en el búfer.

Windows edición 95/Windows 98/Windows Desánimo (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer lo suficientemente grande como para el número de enteros especificado por el *parámetro wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de elementos colocados en el búfer. Si el cuadro de lista es un cuadro de lista de selección única, el valor devuelto es \_ LB ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





