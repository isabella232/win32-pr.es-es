---
title: Mensaje de CB_FINDSTRING (Winuser. h)
description: Busca un elemento que empiece con los caracteres de una cadena especificada en el cuadro de lista de un cuadro combinado.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150269"
---
# <a name="cb_findstring-message"></a>\_Mensaje FINDSTRING CB

Busca un elemento que empiece con los caracteres de una cadena especificada en el cuadro de lista de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que precede al primer elemento que se va a buscar. Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* . Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que contiene los caracteres que se van a buscar. La búsqueda no distingue entre mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del elemento coincidente. Si la búsqueda no se realiza correctamente, se trata de un \_ error CB.

## <a name="remarks"></a>Observaciones

Si crea el cuadro combinado con un estilo dibujado por el propietario, pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , lo que hace el mensaje **\_ FINDSTRING de CB** depende de si la aplicación usa el estilo de [**\_ ordenación CBS**](combo-box-styles.md) . Si usa el estilo **de \_ ordenación CBS** , los mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) se envían al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada. Si no usa el estilo de **\_ ordenación CBS** , el mensaje **CB \_ FINDSTRING** busca un elemento de lista que coincida con el valor del parámetro *lParam* .

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

[**CB \_ FindExactString con**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





