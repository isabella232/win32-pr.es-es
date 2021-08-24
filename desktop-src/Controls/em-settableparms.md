---
title: EM_SETTABLEPARMS mensaje (Richedit.h)
description: Cambia los parámetros de las filas de una tabla.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccb6258f03d76391bf2288331efb3d9ebde4fb903fe907eaa5e9d37e7497a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576355"
---
# <a name="em_settableparms-message"></a>Mensaje \_ DE EM SETTABLEPARMS

Cambia los parámetros de las filas de una tabla.

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



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ ERROR**</dt> </dl>        | No se pueden realizar cambios. Esto puede ocurrir si el control es de texto sin formato o de una sola línea, o si el punto de inserción está dentro de un objeto matemático. También se produce si las tablas están deshabilitadas o si el mensaje [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) establece el **valor SES EX \_ \_ NOTABLE.** <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *wParam o* *lParam* es NULL o apunta a una estructura no válida. El **miembro cCell** de la [**estructura TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe ser al menos 1 y no más de 63. El **miembro cbRow** debe ser `sizeof(TABLEROWPARMS)` igual a o `sizeof(TABLEROWPARMS)   2*sizeof(long)` . El último valor es el tamaño de la estructura **TABLEROWPARMS** de RichEdit 4.1. El **miembro cbCell** de **TABLEROWPARMS** debe ser igual a `sizeof(TABLECELLPARMS)` . El punto de inserción debe estar al principio de una tabla o dentro de una fila de tabla, y el número de celdas solo puede cambiar en una. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente disponible.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentarios

Este mensaje cambia los parámetros del número de filas especificado por el miembro **cRow** de la estructura [**TABLEROWPARMS,**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) si la tabla tiene tantas filas consecutivas. Si **cRow** es menor que 0, el mensaje se itera hasta el final de la tabla. Si el nuevo recuento de celdas difiere del recuento de celdas actual en +1 o 1, inserta o elimina la celda en el índice especificado por el miembro **iCell** de **TABLEROWPARMS.** La fila de la tabla inicial se identifica mediante una posición de carácter. Los miembros **cpStartRow** especifican esta posición con valores mayores o iguales que cero. La posición debe estar dentro de la fila de la tabla, pero no dentro de una tabla anidada, a menos que desee cambiar los parámetros de esa tabla. Si el **miembro cpStartRow** es 1, la selección actual da la posición del carácter. Para ello, coloque la selección en cualquier lugar dentro de la fila de tabla o seleccione la fila con el final activo de la selección al final de la fila de tabla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETTABLEPARMS**](em-gettableparms.md)
</dt> </dl>

 

 





