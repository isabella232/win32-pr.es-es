---
title: LB_GETSEL mensaje (Winuser.h)
description: Obtiene el estado de selección de un elemento.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061880"
---
# <a name="lb_getsel-message"></a>Mensaje \_ LB GETSEL

Obtiene el estado de selección de un elemento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El índice de base cero de un elemento.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se selecciona un elemento, el valor devuelto es mayor que cero; de lo contrario, es cero. Si se produce un error, el valor devuelto es LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





