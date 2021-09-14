---
title: LB_SETCOUNT mensaje (Winuser.h)
description: Establece el recuento de elementos de un cuadro de lista creado con el estilo LBS NODATA y no \_ creado con el estilo \_ HASSTRINGS de LBS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061872"
---
# <a name="lb_setcount-message"></a>Mensaje \_ LB SETCOUNT

Establece el recuento de elementos de un cuadro de lista creado con el estilo [**LBS \_ NODATA**](list-box-styles.md) y no creado con el [**estilo \_ HASSTRINGS de LBS.**](list-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el nuevo recuento de elementos en el cuadro de lista.

Windows edición 95/Windows 98/Windows Desánimo (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ ERR. Si no hay memoria suficiente para almacenar los elementos, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

El **mensaje \_ LB SETCOUNT** solo es compatible con cuadros de lista creados con el estilo [**LBS \_ NODATA**](list-box-styles.md) y no creados con el estilo [**\_ HASSTRINGS de LB.**](list-box-styles.md) Todos los demás cuadros de lista devuelven LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





