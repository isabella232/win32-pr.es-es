---
title: Mensaje de CB_SELECTSTRING (Winuser. h)
description: Busca un elemento que empiece con los caracteres de una cadena especificada en la lista de un cuadro combinado. Si se encuentra un elemento coincidente, se selecciona y se copia en el control de edición.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079357"
---
# <a name="cb_selectstring-message"></a>\_Mensaje SELECTSTRING CB

Busca un elemento que empiece con los caracteres de una cadena especificada en la lista de un cuadro combinado. Si se encuentra un elemento coincidente, se selecciona y se copia en el control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que precede al primer elemento que se va a buscar. Cuando la búsqueda alcanza la parte inferior de la lista, continúa desde la parte superior de la lista hasta el elemento especificado por el parámetro *wParam* . Si *wParam* es-1, se busca en toda la lista desde el principio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que contiene los caracteres que se van a buscar. La búsqueda no distingue entre mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena, el valor devuelto es el índice del elemento seleccionado. Si la búsqueda no se realiza correctamente, el valor devuelto es CB \_ Err y no se cambia la selección actual.

## <a name="remarks"></a>Observaciones

Solo se selecciona una cadena si los caracteres del punto inicial coinciden con los caracteres de la cadena de prefijo.

Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el mensaje **\_ SELECTSTRING de CB** dependerá de si usa el estilo de [**\_ ordenación CBS**](combo-box-styles.md) . Si se usa el estilo de **\_ ordenación CBS** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada. Si no usa el estilo de **\_ ordenación CBS** , **CB \_ SELECTSTRING** intenta coincidir con el valor **DWORD** con el valor del parámetro *lParam* .

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ FindExactString con**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





