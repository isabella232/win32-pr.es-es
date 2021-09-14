---
title: CB_FINDSTRING mensaje (Winuser.h)
description: Busca en el cuadro de lista de un cuadro combinado un elemento que comienza por los caracteres de una cadena especificada.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173969"
---
# <a name="cb_findstring-message"></a>Mensaje \_ FINDSTRING de CB

Busca en el cuadro de lista de un cuadro combinado un elemento que comienza por los caracteres de una cadena especificada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que precede al primer elemento en el que se va a buscar. Cuando la búsqueda llega a la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el *parámetro wParam.* Si *wParam es* -1, se busca todo el cuadro de lista desde el principio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene los caracteres para los que se va a buscar. La búsqueda no distingue mayúsculas de minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del elemento correspondiente. Si la búsqueda no se realiza correctamente, es CB \_ ERR.

## <a name="remarks"></a>Observaciones

Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) lo que haga el mensaje **DE CB \_ FINDSTRING** dependerá de si la aplicación usa el estilo [**\_ CBS SORT.**](combo-box-styles.md) Si usa el estilo SORT de **CBS, \_** los mensajes [**\_ COMPAREITEM**](wm-compareitem.md) de WM se envían al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada. Si no usa el estilo SORT de **CBS, \_** el mensaje **\_ FINDSTRING** de CB busca un elemento de lista que coincida con el valor del *parámetro lParam.*

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

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





