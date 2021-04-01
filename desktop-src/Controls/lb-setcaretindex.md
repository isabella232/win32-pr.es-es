---
title: Mensaje de LB_SETCARETINDEX (Winuser. h)
description: Establece el rectángulo de foco en el elemento en el índice especificado de un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905514"
---
# <a name="lb_setcaretindex-message"></a>\_Mensaje lb SETCARETINDEX

Establece el rectángulo de foco en el elemento en el índice especificado de un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento de cuadro de lista que va a recibir el rectángulo de foco.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Si este valor es **false**, el elemento se desplaza hasta que esté totalmente visible; Si es **true**, el elemento se desplaza hasta que esté al menos parcialmente visible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ Err (-1). De lo contrario, \_ se devuelve lb bien (0).

## <a name="remarks"></a>Observaciones

Si este mensaje se envía a un cuadro de lista de selección única que no contiene un elemento seleccionado, el índice del símbolo de intercalación se establece en el elemento especificado por el parámetro *wParam* . Si el cuadro de lista de selección única contiene un elemento seleccionado, el cuadro de lista devuelve LB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> </dl>

 

 





