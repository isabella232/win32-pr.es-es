---
title: LB_SETHORIZONTALEXTENT mensaje (Winuser.h)
description: Establece el ancho, en píxeles, por el que se puede desplazar horizontalmente un cuadro de lista (el ancho desplazable).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061871"
---
# <a name="lb_sethorizontalextent-message"></a>Mensaje \_ LB SETHORIZONTALEXTENT

Establece el ancho, en píxeles, por el que se puede desplazar horizontalmente un cuadro de lista (el ancho desplazable). Si el ancho del cuadro de lista es menor que este valor, la barra de desplazamiento horizontal desplaza horizontalmente los elementos del cuadro de lista. Si el ancho del cuadro de lista es igual o mayor que este valor, se oculta la barra de desplazamiento horizontal.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número de píxeles por los que se puede desplazar el cuadro de lista.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para responder al mensaje **\_ LB SETHORIZONTALEXTENT,** el cuadro de lista se debe haber definido con el estilo [**\_ HSCROLL de WS.**](/windows/desktop/winmsg/window-styles)

Tenga en cuenta que un cuadro de lista no actualiza dinámicamente su extensión horizontal.

Este mensaje no tiene ningún efecto en un cuadro de lista de varias columnas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md)
</dt> </dl>

 

