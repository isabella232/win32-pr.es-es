---
title: Mensaje de LB_GETSELITEMS (Winuser. h)
description: Rellena un búfer con una matriz de enteros que especifican el número de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996466"
---
# <a name="lb_getselitems-message"></a>\_Mensaje lb GETSELITEMS

Rellena un búfer con una matriz de enteros que especifican el número de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de elementos seleccionados cuyos números de elemento se van a colocar en el búfer.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a un búfer lo suficientemente grande como para el número de enteros especificado por el parámetro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de elementos colocados en el búfer. Si el cuadro de lista es un cuadro de lista de selección única, el valor devuelto es LB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





