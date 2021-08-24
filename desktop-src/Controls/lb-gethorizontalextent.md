---
title: LB_GETHORIZONTALEXTENT mensaje (Winuser.h)
description: Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f754b62ad0f51a236662fdfba2304221d58e1288e2756c0330343c63a0699e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799515"
---
# <a name="lb_gethorizontalextent-message"></a>Mensaje \_ LB GETHORIZONTALEXTENT

Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el ancho desplazable, en píxeles, del cuadro de lista.

## <a name="remarks"></a>Comentarios

Para responder al mensaje **\_ LB GETHORIZONTALEXTENT,** el cuadro de lista se debe haber definido con el estilo [**\_ HSCROLL de WS.**](/windows/desktop/winmsg/window-styles)

Si la aplicación no establece la extensión horizontal del cuadro de lista (mediante [**LB \_ SETHORIZONTALEXTENT),**](lb-sethorizontalextent.md)la extensión horizontal predeterminada es cero. Tenga en cuenta que el cuadro de lista no actualiza dinámicamente su extensión horizontal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

