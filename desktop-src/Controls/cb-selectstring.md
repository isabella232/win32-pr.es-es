---
title: CB_SELECTSTRING mensaje (Winuser.h)
description: Busca en la lista de un cuadro combinado un elemento que comienza con los caracteres de una cadena especificada. Si se encuentra un elemento correspondiente, se selecciona y se copia en el control de edición.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING controles de Windows mensaje
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
ms.openlocfilehash: 4bedef20646664e37405c97a97f9e49147cad8acc08c05e33172e44a34298f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019973"
---
# <a name="cb_selectstring-message"></a>Mensaje \_ SELECTSTRING de CB

Busca en la lista de un cuadro combinado un elemento que comienza con los caracteres de una cadena especificada. Si se encuentra un elemento correspondiente, se selecciona y se copia en el control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que precede al primer elemento en el que se va a buscar. Cuando la búsqueda llega a la parte inferior de la lista, continúa desde la parte superior de la lista hasta el elemento especificado por el *parámetro wParam.* Si *wParam* es -1, se busca toda la lista desde el principio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene los caracteres para los que se va a buscar. La búsqueda no distingue mayúsculas de minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena, el valor devuelto es el índice del elemento seleccionado. Si la búsqueda no se realiza correctamente, el valor devuelto es CB \_ ERR y la selección actual no cambia.

## <a name="remarks"></a>Comentarios

Solo se selecciona una cadena si los caracteres del punto inicial coinciden con los caracteres de la cadena de prefijo.

Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) lo que haga el mensaje **\_ SELECTSTRING** de CB dependerá de si usa el estilo [**CBS \_ SORT.**](combo-box-styles.md) Si se usa el estilo SORT de **CBS, \_** el sistema envía mensajes [**\_ COMPAREITEM**](wm-compareitem.md) de WM al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada. Si no usa el estilo SORT de **CBS, \_** **CB \_ SELECTSTRING** intenta hacer coincidir el valor **DWORD** con el valor del *parámetro lParam.*

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





