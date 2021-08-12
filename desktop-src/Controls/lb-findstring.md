---
title: LB_FINDSTRING mensaje (Winuser.h)
description: Busca la primera cadena en un cuadro de lista que comienza con la cadena especificada.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a4eb2abbff27c6bde6a4bb44d0faa192ca75229be657bd787aa437b243cd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671308"
---
# <a name="lb_findstring-message"></a>Mensaje \_ LB FINDSTRING

Busca la primera cadena en un cuadro de lista que comienza con la cadena especificada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento situado delante del primer elemento que se va a buscar. Cuando la búsqueda llega a la parte inferior del cuadro de lista, continúa buscando desde la parte superior del cuadro de lista hasta el elemento especificado por el *parámetro wParam.* Si *wParam es* -1, se busca todo el cuadro de lista desde el principio.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene la cadena para la que se va a buscar. La búsqueda es independiente de mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice del elemento correspondiente o \_ LB ERR si la búsqueda no se ha hecho correctamente.

## <a name="remarks"></a>Observaciones

Si el cuadro de lista tiene el estilo dibujado por el propietario, pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, la acción realizada por **LB \_ FINDSTRING** depende de si se usa el estilo SORT de [**LBS. \_**](list-box-styles.md) Si **se usa SORT de \_ LBS,** el sistema envía mensajes [**\_ COMPAREITEM**](wm-compareitem.md) de WM al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada. De lo contrario, **LB \_ FINDSTRING** intenta encontrar un elemento que tenga un valor largo (proporcionado como el parámetro *lParam* del mensaje [**LB \_ ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING)**](lb-insertstring.md) que coincida con el parámetro *lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)
</dt> </dl>

 

 





