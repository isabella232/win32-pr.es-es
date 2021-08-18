---
title: EM_GETTABLEPARMS mensaje (Richedit.h)
description: Recupera los parámetros de tabla para una fila de tabla y los parámetros de celda para el número especificado de celdas.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS controles de Windows mensaje
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
ms.openlocfilehash: c2ddca96ce29a0f7b7076580b48cfeceecf1f638830b7c77bc9406a39e97de57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545035"
---
# <a name="em_gettableparms-message"></a>Mensaje \_ GETTABLEPARMS de EM

Recupera los parámetros de tabla para una fila de tabla y los parámetros de celda para el número especificado de celdas.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura TABLEROWPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TABLECELLPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o uno de los siguientes códigos de error.



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | No se pueden realizar cambios. Esto puede ocurrir si el control es de texto sin formato o de una sola línea, o si el punto de inserción está dentro de un objeto matemático. También se produce si las tablas están deshabilitadas si el [**mensaje EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) establece **el valor SES EX \_ \_ NOTABLE.** <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *wParam o* *lParam* es NULL o apunta a una estructura no válida. El **miembro cbRow** de la [**estructura TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe ser igual o `sizeof(TABLEROWPARMS)` sizeof(TABLEROWPARMS) 2 \* sizeof(long). El último valor es el tamaño de la estructura **TABLEROWPARMS** de RichEdit 4.1. El **miembro cbCell** de la **estructura TABLEROWPARMS** debe ser igual `sizeof(TABLECELLPARMS)` a . La posición del carácter de consulta debe estar en un delimitador de fila de tabla. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente disponible.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentarios

Este mensaje obtiene los parámetros de tabla de la fila en la posición de carácter especificada por el miembro **cpStartRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) y el número de **celdas especificadas** por el miembro cCells de la [**estructura TABLECELLPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)

La posición de carácter especificada por el miembro **cpStartRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe estar al principio de la fila de la tabla o al final del delimitador de la fila de la tabla. Si **cpStartRow** se establece en 1, la selección actual da la posición del carácter. En este caso, coloque la selección al final de la fila (entre la marca de celda y el delimitador final de la fila de tabla) o seleccione la fila.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETTABLEPARMS**](em-settableparms.md)
</dt> </dl>

 

 





