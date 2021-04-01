---
title: Mensaje de LB_SELITEMRANGEEX (Winuser. h)
description: Selecciona uno o más elementos consecutivos en un cuadro de lista de selección múltiple.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996923"
---
# <a name="lb_selitemrangeex-message"></a>\_Mensaje lb SELITEMRANGEEX

Selecciona uno o más elementos consecutivos en un cuadro de lista de selección múltiple.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del primer elemento que se va a seleccionar.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el índice de base cero del último elemento que se va a seleccionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ Err.

## <a name="remarks"></a>Observaciones

Si el parámetro *wParam* es menor que el parámetro *lParam* , se selecciona el intervalo de elementos especificado. Si *wParam* es mayor o igual que *lParam*, el intervalo se quita del intervalo de elementos especificado. Para seleccionar solo un elemento, seleccione dos elementos y, a continuación, anule la selección del elemento no deseado.

Use este mensaje solo con cuadros de lista de selección múltiple.

Este mensaje puede seleccionar un intervalo solo dentro de los primeros 65.536 elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





