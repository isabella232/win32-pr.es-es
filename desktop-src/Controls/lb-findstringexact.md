---
title: Mensaje de LB_FINDSTRINGEXACT (Winuser. h)
description: Busca la primera cadena del cuadro de lista que coincide exactamente con la cadena especificada, salvo que la búsqueda no distingue entre mayúsculas y minúsculas.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- LB_FINDSTRINGEXACT controles de mensajes de Windows
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
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079720"
---
# <a name="lb_findstringexact-message"></a>\_Mensaje lb FindExactString con

Busca la primera cadena del cuadro de lista que coincide exactamente con la cadena especificada, salvo que la búsqueda no distingue entre mayúsculas y minúsculas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento situado delante del primer elemento que se va a buscar. Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa realizando una búsqueda desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* . Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que se va a buscar. La búsqueda no distingue entre mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del elemento coincidente, o LB \_ Err si la búsqueda no se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

Esta función solo se realiza correctamente si la cadena especificada y un elemento de cuadro de lista tienen la misma longitud (excepto el valor null al final de la cadena especificada) y tienen exactamente los mismos caracteres.

Si el cuadro de lista tiene el estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , la acción realizada por **lb \_ FindExactString con** dependerá de si se usa el estilo de [**\_ ordenación lbs**](list-box-styles.md) . Si se usa la **\_ ordenación lb** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada. De lo contrario, **lb \_ FindExactString con** intenta encontrar un elemento que tiene un valor Long (proporcionado como el parámetro *lParam* del [**mensaje \_ lb**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) que coincide con el parámetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ FINDSTRING**](lb-findstring.md)
</dt> </dl>

 

 





