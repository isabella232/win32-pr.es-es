---
title: Mensaje de LB_SETHORIZONTALEXTENT (Winuser. h)
description: Establece el ancho, en píxeles, por el que se puede desplazar un cuadro de lista horizontalmente (el ancho desplazable).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905513"
---
# <a name="lb_sethorizontalextent-message"></a>\_Mensaje lb SETHORIZONTALEXTENT

Establece el ancho, en píxeles, por el que se puede desplazar un cuadro de lista horizontalmente (el ancho desplazable). Si el ancho del cuadro de lista es menor que este valor, la barra de desplazamiento horizontal se desplaza horizontalmente por los elementos del cuadro de lista. Si el ancho del cuadro de lista es igual o mayor que este valor, se oculta la barra de desplazamiento horizontal.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número de píxeles que se puede desplazar el cuadro de lista.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para responder al mensaje de **lb \_ SETHORIZONTALEXTENT** , el cuadro de lista se debe haber definido con el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Tenga en cuenta que un cuadro de lista no actualiza dinámicamente su extensión horizontal.

Este mensaje no tiene ningún efecto en un cuadro de lista de varias columnas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md)
</dt> </dl>

 

