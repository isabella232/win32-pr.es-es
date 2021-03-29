---
title: Mensaje de LB_GETTEXT (Winuser. h)
description: Obtiene una cadena de un cuadro de lista.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT controles de mensajes de Windows
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
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492149"
---
# <a name="lb_gettext-message"></a>Mensaje de LB \_ GETTEXT

Obtiene una cadena de un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena que se va a recuperar.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibirá la cadena; es de tipo **LPTSTR** que se convierte posteriormente en **lParam**. El búfer debe tener espacio suficiente para la cadena y un carácter nulo de terminación. Se puede enviar un mensaje de [**lb \_ GETTEXTLEN**](lb-gettextlen.md) antes del mensaje de la extensión de **equilibro de lb \_** para recuperar la longitud, en **TCHAR** s, de la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación. Si *wParam* no especifica un índice válido, el valor devuelto es lb \_ Err.

## <a name="remarks"></a>Observaciones

Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , el búfer al que apunta el parámetro *lParam* recibe el valor asociado al elemento (los datos del elemento).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETTEXTLEN**](lb-gettextlen.md)
</dt> </dl>

 

 





