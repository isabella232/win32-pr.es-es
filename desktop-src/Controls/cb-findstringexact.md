---
title: CB_FINDSTRINGEXACT mensaje (Winuser.h)
description: Busca la primera cadena de cuadro de lista en un cuadro combinado que coincide con la cadena especificada en el parámetro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173966"
---
# <a name="cb_findstringexact-message"></a>Mensaje \_ FINDSTRINGEXACT de CB

Busca la primera cadena de cuadro de lista en un cuadro combinado que coincide con la cadena especificada en el *parámetro lParam.*

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que precede al primer elemento en el que se va a buscar. Cuando la búsqueda llega a la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el *parámetro wParam.* Si *wParam es* -1, se busca todo el cuadro de lista desde el principio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL para la que se va a buscar. La búsqueda no distingue mayúsculas de minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del elemento correspondiente. Si la búsqueda no se realiza correctamente, es CB \_ ERR.

## <a name="remarks"></a>Observaciones

Esta función se realiza correctamente solo si la cadena especificada y un elemento de cuadro combinado tienen la misma longitud (excepto para el carácter nulo de terminación) y los mismos caracteres.

Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) la funcionalidad del mensaje **\_ FINDSTRINGEXACT** de CB depende de si la aplicación usa el estilo [**\_ CBS SORT.**](combo-box-styles.md) Si usa el estilo SORT de **CBS, \_** los mensajes [**\_ COMPAREITEM**](wm-compareitem.md) de WM se envían al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada. Si no usa el estilo SORT de **CBS, \_** el mensaje **\_ FINDSTRINGEXACT** de CB busca un elemento de lista que coincida con el valor del *parámetro lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





