---
title: Mensaje de LB_SELECTSTRING (Winuser. h)
description: Busca un elemento que empiece con los caracteres de una cadena especificada en un cuadro de lista. Si se encuentra un elemento coincidente, se selecciona el elemento.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492442"
---
# <a name="lb_selectstring-message"></a>\_Mensaje lb SELECTSTRING

Busca un elemento que empiece con los caracteres de una cadena especificada en un cuadro de lista. Si se encuentra un elemento coincidente, se selecciona el elemento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento situado delante del primer elemento que se va a buscar. Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* . Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que contiene el prefijo que se va a buscar. La búsqueda es independiente de las mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la búsqueda se realiza correctamente, el valor devuelto es el índice del elemento seleccionado. Si no se realiza la búsqueda, el valor devuelto es LB \_ Err y no se cambia la selección actual.

## <a name="remarks"></a>Observaciones

Si es necesario, el cuadro de lista se desplaza para que el elemento seleccionado se muestre en la vista.

No use este mensaje con un cuadro de lista que tenga los estilos [**lb \_ MULTIPLESEL**](list-box-styles.md) o [**lb \_ EXTENDEDSEL**](list-box-styles.md) .

Un elemento se selecciona solo si sus caracteres iniciales del punto inicial coinciden con los caracteres de la cadena especificada por el parámetro *lParam* .

Si el cuadro de lista tiene el estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , la acción realizada por **lb \_ SELECTSTRING** dependerá de si se usa el estilo de [**\_ ordenación lbs**](list-box-styles.md) . Si se usa la **\_ ordenación lb** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada. De lo contrario, **lb \_ SELECTSTRING** intenta encontrar un elemento que tiene un valor Long (proporcionado como el parámetro *lParam* del [**mensaje \_ lb**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) que coincide con el parámetro *lParam* .

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ FINDSTRING**](lb-findstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





