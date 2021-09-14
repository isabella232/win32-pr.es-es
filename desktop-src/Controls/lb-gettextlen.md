---
title: LB_GETTEXTLEN mensaje (Winuser.h)
description: Obtiene la longitud de una cadena en un cuadro de lista.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061877"
---
# <a name="lb_gettextlen-message"></a>Lb \_ GETTEXTLEN message

Obtiene la longitud de una cadena en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena.

Windows edición 95/Windows 98/Windows Desánimo (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la longitud de la cadena, en **TCHAR,** sin incluir el carácter nulo final. En determinadas condiciones, este valor puede ser realmente mayor que la longitud del texto. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

Si el *parámetro wParam* no especifica un índice válido, el valor devuelto es LB \_ ERR.

## <a name="remarks"></a>Observaciones

En determinadas condiciones, el valor devuelto es mayor que la longitud real del texto. Esto se produce con ciertas mezclas de ANSI y Unicode, y se debe al sistema operativo que permite la posible existencia de caracteres de juego de caracteres de doble byte (DBCS) dentro del texto. Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; Por lo tanto, siempre se puede usar para guiar la asignación del búfer. Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y diálogos comunes, que usan Unicode.

Para obtener la longitud exacta del texto, use los mensajes [**WM \_ GETTEXT,**](/windows/desktop/winmsg/wm-gettext) [**LB \_ GETTEXT**](lb-gettext.md)o [**CB \_ GETLBTEXT,**](cb-getlbtext.md) o la [**función GetWindowText.**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)

Si el cuadro de lista tiene un estilo dibujado por el propietario, pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, el valor devuelto siempre es el tamaño, en bytes, de **un DWORD**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETLBTEXT**](cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](lb-gettext.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

