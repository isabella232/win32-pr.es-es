---
title: Mensaje de CB_GETLBTEXTLEN (Winuser. h)
description: Obtiene la longitud, en caracteres, de una cadena en la lista de un cuadro combinado.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN controles de mensajes de Windows
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
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996377"
---
# <a name="cb_getlbtextlen-message"></a>\_Mensaje GETLBTEXTLEN CB

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

El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación. Si una cadena ANSI es el número de bytes, y si es una cadena Unicode, es el número de caracteres. En determinadas condiciones, este valor puede ser realmente mayor que la longitud del texto. Para obtener más información, vea la sección Comentarios.

Si el parámetro *wParam* no especifica un índice válido, el valor devuelto es CB \_ Err.

## <a name="remarks"></a>Observaciones

En determinadas condiciones, el valor devuelto es mayor que la longitud real del texto. Esto sucede con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema operativo permite la existencia de caracteres de juegos de caracteres de doble byte (DBCS) en el texto. Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; por lo tanto, siempre puede usarlo para guiar la asignación de búfer. Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y cuadros de diálogo comunes, que usan Unicode.

Para obtener la longitud exacta del texto, use los mensajes [**de \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) , o la función [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

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

 

