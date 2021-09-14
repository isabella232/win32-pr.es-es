---
title: LB_GETCOUNT mensaje (Winuser.h)
description: Obtiene el número de elementos de un cuadro de lista.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061893"
---
# <a name="lb_getcount-message"></a>Mensaje \_ GETCOUNT de LB

Obtiene el número de elementos de un cuadro de lista.

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

El valor devuelto es el número de elementos del cuadro de lista o \_ LB ERR si se produce un error.

## <a name="remarks"></a>Observaciones

El recuento devuelto es uno mayor que el valor de índice del último elemento (el índice está basado en cero).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ SETCOUNT**](lb-setcount.md)
</dt> </dl>

 

 





