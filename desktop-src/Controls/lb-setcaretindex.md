---
title: LB_SETCARETINDEX mensaje (Winuser.h)
description: Establece el rectángulo de foco en el elemento situado en el índice especificado en un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.
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
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061873"
---
# <a name="lb_setcaretindex-message"></a>Mensaje \_ LB SETCARETINDEX

Establece el rectángulo de foco en el elemento situado en el índice especificado en un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento de cuadro de lista que va a recibir el rectángulo de foco.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Si este valor es **FALSE,** el elemento se desplaza hasta que está totalmente visible; Si es **TRUE,** el elemento se desplaza hasta que esté al menos parcialmente visible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es \_ LB ERR (-1). De lo contrario, \_ se devuelve LB OKAY (0).

## <a name="remarks"></a>Observaciones

Si este mensaje se envía a un cuadro de lista de selección única que no contiene un elemento seleccionado, el índice de signo de referencia se establece en el elemento especificado por el *parámetro wParam.* Si el cuadro de lista de selección única contiene un elemento seleccionado, el cuadro de lista devuelve LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> </dl>

 

 





