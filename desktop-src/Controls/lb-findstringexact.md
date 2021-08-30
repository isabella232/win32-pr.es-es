---
title: LB_FINDSTRINGEXACT mensaje (Winuser.h)
description: Busca la primera cadena de cuadro de lista que coincida exactamente con la cadena especificada, salvo que la búsqueda no distingue mayúsculas de minúsculas.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- LB_FINDSTRINGEXACT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a9b9f5a5562e1d78da87a928d8b5c319c3cee634bbed6a37891fbe35cf148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085535"
---
# <a name="lb_findstringexact-message"></a>Mensaje \_ LB FINDSTRINGEXACT

Busca la primera cadena de cuadro de lista que coincida exactamente con la cadena especificada, salvo que la búsqueda no distingue mayúsculas de minúsculas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento situado delante del primer elemento que se va a buscar. Cuando la búsqueda llega a la parte inferior del cuadro de lista, continúa buscando desde la parte superior del cuadro de lista hasta el elemento especificado por el *parámetro wParam.* Si *wParam es* -1, se busca todo el cuadro de lista desde el principio.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL para la que se va a buscar. La búsqueda no distingue mayúsculas de minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del elemento correspondiente o LB ERR si la \_ búsqueda no se ha hecho correctamente.

## <a name="remarks"></a>Comentarios

Esta función solo se realiza correctamente si la cadena especificada y un elemento de cuadro de lista tienen la misma longitud (excepto el valor NULL al final de la cadena especificada) y tienen exactamente los mismos caracteres.

Si el cuadro de lista tiene el estilo dibujado por el propietario, pero no el estilo [**\_ LBS HASSTRINGS,**](list-box-styles.md) la acción realizada por **LB \_ FINDSTRINGEXACT** depende de si se usa el estilo [**SORT \_ de LBS.**](list-box-styles.md) Si **se usa SORT de \_ LBS,** el sistema envía mensajes [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada. De lo contrario, **LB \_ FINDSTRINGEXACT** intenta encontrar un elemento que tenga un valor long (proporcionado como parámetro *lParam* del mensaje [**LB \_ ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING)**](lb-insertstring.md) que coincida con el parámetro *lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ FINDSTRING**](lb-findstring.md)
</dt> </dl>

 

 





