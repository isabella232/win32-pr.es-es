---
title: Mensaje de LB_GETTEXTLEN (Winuser. h)
description: Obtiene la longitud de una cadena en un cuadro de lista.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150195"
---
# <a name="lb_gettextlen-message"></a>\_Mensaje lb GETTEXTLEN

Obtiene la longitud de una cadena en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación. En determinadas condiciones, este valor puede ser realmente mayor que la longitud del texto. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

Si el parámetro *wParam* no especifica un índice válido, el valor devuelto es lb \_ Err.

## <a name="remarks"></a>Observaciones

En determinadas condiciones, el valor devuelto es mayor que la longitud real del texto. Esto sucede con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema operativo permite la existencia de caracteres de juegos de caracteres de doble byte (DBCS) en el texto. Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; por tanto, se puede usar siempre para guiar la asignación de búfer. Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y cuadros de diálogo comunes, que usan Unicode.

Para obtener la longitud exacta del texto, use los mensajes [**de \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) , o la función [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

Si el cuadro de lista tiene un estilo dibujado por el propietario, pero no el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) , el valor devuelto siempre es el tamaño, en bytes, de un valor **DWORD**.

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

[**CB \_ GETLBTEXT**](cb-getlbtext.md)
</dt> <dt>

[**\_apgettext GETTEXT**](lb-gettext.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GETTEXT de WM \_**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

