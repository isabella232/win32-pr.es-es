---
title: LB_SETCOUNT mensaje (Winuser.h)
description: Establece el recuento de elementos de un cuadro de lista creado con el estilo LBS NODATA y no creado con el estilo \_ \_ HASSTRINGS de LBS.
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
ms.openlocfilehash: 2e1b3f68a67de2b7caa77cfd7c9e6f2a5b164e20af42100882fef1aad04eca14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433951"
---
# <a name="lb_setcount-message"></a>Mensaje \_ LB SETCOUNT

Establece el recuento de elementos de un cuadro de lista creado con el estilo [**LBS \_ NODATA**](list-box-styles.md) y no creado con el [**estilo \_ HASSTRINGS de LBS.**](list-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el nuevo recuento de elementos en el cuadro de lista.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ ERR. Si no hay memoria suficiente para almacenar los elementos, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

El **mensaje \_ LB SETCOUNT** solo es compatible con cuadros de lista creados con el estilo [**LBS \_ NODATA**](list-box-styles.md) y no creados con el [**estilo \_ HASSTRINGS de LB.**](list-box-styles.md) Todos los demás cuadros de lista devuelven LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





