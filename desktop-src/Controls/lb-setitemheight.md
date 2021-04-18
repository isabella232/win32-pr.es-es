---
title: Mensaje de LB_SETITEMHEIGHT (Winuser. h)
description: Establece el alto, en píxeles, de los elementos de un cuadro de lista. Si el cuadro de lista tiene el \_ estilo lbs OWNERDRAWVARIABLE, este mensaje establece el alto del elemento especificado por el parámetro wParam. De lo contrario, este mensaje establece el alto de todos los elementos del cuadro de lista.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT controles de mensajes de Windows
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
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492431"
---
# <a name="lb_setitemheight-message"></a>\_Mensaje lb SETITEMHEIGHT

Establece el alto, en píxeles, de los elementos de un cuadro de lista. Si el cuadro de lista tiene el estilo [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) , este mensaje establece el alto del elemento especificado por el parámetro *wParam* . De lo contrario, este mensaje establece el alto de todos los elementos del cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento en el cuadro de lista. Use este parámetro solo si el cuadro de lista tiene el estilo [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) ; de lo contrario, establézcalo en cero.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el alto, en píxeles, del elemento. El alto máximo es de 255 píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el índice o el alto no son válidos, el valor devuelto es LB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)
</dt> </dl>

 

 





