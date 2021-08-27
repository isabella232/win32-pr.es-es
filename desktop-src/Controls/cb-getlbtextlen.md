---
title: CB_GETLBTEXTLEN mensaje (Winuser.h)
description: Obtiene la longitud, en caracteres, de una cadena en la lista de un cuadro combinado.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb226a9012d9573e17bd88a114ebcd2b96e406a38208cc78a925bdca976cd4b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089155"
---
# <a name="cb_getlbtextlen-message"></a>Mensaje \_ GETLBTEXTLEN de CB

Obtiene la longitud, en caracteres, de una cadena en la lista de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la longitud de la cadena, en **TCHAR,** sin incluir el carácter nulo final. Si una cadena ANSI es el número de bytes y si es una cadena Unicode, es el número de caracteres. En determinadas condiciones, este valor puede ser realmente mayor que la longitud del texto. Para obtener más información, vea la sección Comentarios.

Si el *parámetro wParam* no especifica un índice válido, el valor devuelto es CB \_ ERR.

## <a name="remarks"></a>Comentarios

En determinadas condiciones, el valor devuelto es mayor que la longitud real del texto. Esto se produce con ciertas mezclas de ANSI y Unicode, y se debe al sistema operativo que permite la posible existencia de caracteres de juego de caracteres de doble byte (DBCS) dentro del texto. Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; para que siempre pueda usarlo para guiar la asignación del búfer. Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y diálogos comunes, que usan Unicode.

Para obtener la longitud exacta del texto, use los mensajes [**WM \_ GETTEXT,**](/windows/desktop/winmsg/wm-gettext) [**LB \_ GETTEXT**](lb-gettext.md)o [**CB \_ GETLBTEXT,**](cb-getlbtext.md) o la [**función GetWindowText.**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

