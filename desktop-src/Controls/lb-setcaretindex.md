---
title: LB_SETCARETINDEX mensaje (Winuser.h)
description: Establece el rectángulo de foco en el elemento en el índice especificado en un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362a24dbaf27ed8a92a8df2ba85e26bb535ee73eed57d13e72d2670ce9f80b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433995"
---
# <a name="lb_setcaretindex-message"></a>Mensaje \_ LB SETCARETINDEX

Establece el rectángulo de foco en el elemento en el índice especificado en un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento de cuadro de lista que va a recibir el rectángulo de foco.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Si este valor es **FALSE**, el elemento se desplaza hasta que está totalmente visible; si es **TRUE**, el elemento se desplaza hasta que sea al menos parcialmente visible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es \_ LB ERR (-1). De lo contrario, \_ se devuelve LB OKAY (0).

## <a name="remarks"></a>Observaciones

Si este mensaje se envía a un cuadro de lista de selección única que no contiene un elemento seleccionado, el índice del signo de referencia se establece en el elemento especificado por el *parámetro wParam.* Si el cuadro de lista de selección única contiene un elemento seleccionado, el cuadro de lista devuelve LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> </dl>

 

 





