---
title: Mensaje de LB_GETITEMRECT (Winuser. h)
description: Obtiene las dimensiones del rectángulo que delimita un elemento de cuadro de lista tal como se muestra actualmente en el cuadro de lista.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490205"
---
# <a name="lb_getitemrect-message"></a>\_Mensaje lb GETITEMRECT

Obtiene las dimensiones del rectángulo que delimita un elemento de cuadro de lista tal como se muestra actualmente en el cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El índice de base cero de un elemento.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá las coordenadas de cliente para el elemento en el cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

