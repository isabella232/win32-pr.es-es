---
title: LB_SETITEMHEIGHT mensaje (Winuser.h)
description: Establece el alto, en píxeles, de los elementos de un cuadro de lista. Si el cuadro de lista tiene el estilo LBS OWNERDRAWVARIABLE, este mensaje establece el alto del elemento \_ especificado por el parámetro wParam. De lo contrario, este mensaje establece el alto de todos los elementos del cuadro de lista.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd661c9fb32d2cbe0763f8c138d133f8a32b46d17201b33033b832aeb8cb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433881"
---
# <a name="lb_setitemheight-message"></a>Mensaje \_ DE LB SETITEMHEIGHT

Establece el alto, en píxeles, de los elementos de un cuadro de lista. Si el cuadro de lista tiene el estilo [**LBS \_ OWNERDRAWVARIABLE,**](list-box-styles.md) este mensaje establece el alto del elemento especificado por el *parámetro wParam.* De lo contrario, este mensaje establece el alto de todos los elementos del cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento en el cuadro de lista. Use este parámetro solo si el cuadro de lista tiene el estilo [**LBS \_ OWNERDRAWVARIABLE;**](list-box-styles.md) de lo contrario, esta establezca en cero.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el alto, en píxeles, del elemento. El alto máximo es de 255 píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el índice o alto no es válido, el valor devuelto es \_ LB ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)
</dt> </dl>

 

 





