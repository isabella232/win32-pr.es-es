---
title: LB_SELECTSTRING mensaje (Winuser.h)
description: Busca en un cuadro de lista un elemento que comienza con los caracteres de una cadena especificada. Si se encuentra un elemento correspondiente, se selecciona el elemento .
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING controles de Windows mensaje
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
ms.openlocfilehash: 848a0935a1ca4d3ce717fecae3de76f57e36091ba084041aa9d012d6318a269a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434085"
---
# <a name="lb_selectstring-message"></a>Mensaje \_ SELECTSTRING de LB

Busca en un cuadro de lista un elemento que comienza con los caracteres de una cadena especificada. Si se encuentra un elemento correspondiente, se selecciona el elemento .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento situado delante del primer elemento que se va a buscar. Cuando la búsqueda llega a la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el *parámetro wParam.* Si *wParam es* -1, se busca todo el cuadro de lista desde el principio.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene el prefijo para el que se va a buscar. La búsqueda es independiente de mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la búsqueda se realiza correctamente, el valor devuelto es el índice del elemento seleccionado. Si la búsqueda no se realiza correctamente, el valor devuelto es \_ LB ERR y no se cambia la selección actual.

## <a name="remarks"></a>Comentarios

El cuadro de lista se desplaza, si es necesario, para que el elemento seleccionado se vea.

No use este mensaje con un cuadro de lista que tenga los estilos [**LBS \_ MULTIPLESEL**](list-box-styles.md) o [**LBS \_ EXTENDEDSEL.**](list-box-styles.md)

Solo se selecciona un elemento si sus caracteres iniciales del punto inicial coinciden con los caracteres de la cadena especificada por el *parámetro lParam.*

Si el cuadro de lista tiene el estilo dibujado por el propietario, pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, la acción realizada por **LB \_ SELECTSTRING** depende de si se usa el estilo [**SORT \_ de LBS.**](list-box-styles.md) Si **se usa SORT de \_ LBS,** el sistema envía mensajes [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada. De lo contrario, **LB \_ SELECTSTRING** intenta encontrar un elemento que tenga un valor largo (proporcionado como el parámetro *lParam* del mensaje [**LB \_ ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING)**](lb-insertstring.md) que coincida con el parámetro *lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

 

 





