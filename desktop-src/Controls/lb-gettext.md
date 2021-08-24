---
title: LB_GETTEXT mensaje (Winuser.h)
description: Obtiene una cadena de un cuadro de lista.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2aa37a2d07e440aac615d1edc1e6f91c6a60e71a96418cd443daff9809ec18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434105"
---
# <a name="lb_gettext-message"></a>Mensaje \_ GETTEXT de LB

Obtiene una cadena de un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena que se recuperará.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibirá la cadena; es de tipo **LPTSTR,** que posteriormente se convierte en **un LPARAM.** El búfer debe tener espacio suficiente para la cadena y un carácter nulo de terminación. Se [**puede enviar un mensaje LB \_ GETTEXTLEN**](lb-gettextlen.md) antes del mensaje **LB \_ GETTEXT** para recuperar la longitud, en **TCHAR,** de la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la longitud de la cadena, en **TCHAR,** sin incluir el carácter nulo de terminación. Si *wParam no* especifica un índice válido, el valor devuelto es LB \_ ERR.

## <a name="remarks"></a>Observaciones

Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, el búfer al que apunta el parámetro *lParam* recibe el valor asociado al elemento (los datos del elemento).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETTEXTLEN**](lb-gettextlen.md)
</dt> </dl>

 

 





