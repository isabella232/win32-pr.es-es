---
title: Mensaje EM_GETTABLEPARMS (RichEdit. h)
description: Recupera los parámetros de tabla para una fila de tabla y los parámetros de celda para el número de celdas especificado.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905199"
---
# <a name="em_gettableparms-message"></a>\_Mensaje GETTABLEPARMS em

Recupera los parámetros de tabla para una fila de tabla y los parámetros de celda para el número de celdas especificado.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o uno de los siguientes códigos de error.



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ ERROR**</dt> </dl>        | No se pueden realizar cambios. Esto puede ocurrir si el control es un control de texto sin formato o de una sola línea, o si el punto de inserción está dentro de un objeto matemático. También se produce si las tablas están deshabilitadas si el mensaje [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) establece el valor **\_ \_ importante de SES** . <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* o *lParam* es null o apunta a una estructura no válida. El miembro **cbRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe ser igual `sizeof(TABLEROWPARMS)` o sizeof (TABLEROWPARMS) 2 \* sizeof (Long). El último valor es el tamaño de la estructura **TABLEROWPARMS** de RichEdit 4,1. El miembro **cbCell** de la estructura **TABLEROWPARMS** debe ser igual a `sizeof(TABLECELLPARMS)` . La posición del carácter de la consulta debe estar en un delimitador de filas de la tabla. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Este mensaje obtiene los parámetros de tabla para la fila en la posición de caracteres especificada por el miembro **cpStartRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) y el número de celdas especificadas por el miembro **cCells** de la estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

La posición de caracteres especificada por el miembro **cpStartRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe estar al principio de la fila de la tabla o en el delimitador final de la fila de la tabla. Si **cpStartRow** se establece en 1, la selección actual proporciona la posición del carácter. En este caso, coloque la selección al final de la fila (entre la marca de celda y el delimitador final de la fila de la tabla) o seleccione la fila.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETTABLEPARMS em**](em-settableparms.md)
</dt> </dl>

 

 





