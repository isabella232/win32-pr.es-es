---
title: Mensaje de LB_SETCOUNT (Winuser. h)
description: Establece el recuento de elementos de un cuadro de lista creado con el \_ estilo lbs NoData y no se creó con el \_ estilo lb HASSTRINGS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079657"
---
# <a name="lb_setcount-message"></a>\_Mensaje lb SETCOUNT

Establece el recuento de elementos de un cuadro de lista creado con el estilo [**lbs \_ NoData**](list-box-styles.md) y no se creó con el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el nuevo recuento de elementos del cuadro de lista.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ Err. Si no hay memoria suficiente para almacenar los elementos, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

El mensaje **lb \_ SETCOUNT** solo se admite en los cuadros de lista creados con el estilo [**lbs \_ NoData**](list-box-styles.md) y no se crean con el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) . El resto de los cuadros de lista devuelven LB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





