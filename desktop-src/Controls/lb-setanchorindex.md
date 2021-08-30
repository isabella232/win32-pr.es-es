---
title: LB_SETANCHORINDEX mensaje (Winuser.h)
description: Establece el elemento delimitador \ 8212; es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos desde el elemento delimitador hasta el elemento de careta.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- LB_SETANCHORINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d8e1eba4168cfd6dd9a7e18a5b82b252c08908e9e49ce7059ed8fdef5ea95d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085355"
---
# <a name="lb_setanchorindex-message"></a>Mensaje \_ LB SETANCHORINDEX

Establece el elemento delimitador, es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos desde el elemento delimitador hasta el elemento de careta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice del nuevo elemento delimitador.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es \_ LB ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)
</dt> </dl>

 

 





