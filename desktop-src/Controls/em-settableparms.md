---
title: Mensaje EM_SETTABLEPARMS (RichEdit. h)
description: Cambia los parámetros de las filas de una tabla.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS controles de mensajes de Windows
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
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996223"
---
# <a name="em_settableparms-message"></a>\_Mensaje SETTABLEPARMS em

Cambia los parámetros de las filas de una tabla.

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



| Código devuelto                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ ERROR**</dt> </dl>        | No se pueden realizar cambios. Esto puede ocurrir si el control es un control de texto sin formato o de una sola línea, o si el punto de inserción está dentro de un objeto matemático. También se produce si las tablas están deshabilitadas o si el mensaje [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) establece el valor **\_ \_ importante de SES** . <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* o *lParam* es null o apunta a una estructura no válida. El miembro **cCell** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe ser al menos 1 y no superior a 63. El miembro **cbRow** debe ser igual a `sizeof(TABLEROWPARMS)` o `sizeof(TABLEROWPARMS)   2*sizeof(long)` . El último valor es el tamaño de la estructura **TABLEROWPARMS** de RichEdit 4,1. El miembro **cbCell** de **TABLEROWPARMS** debe ser igual a `sizeof(TABLECELLPARMS)` . El punto de inserción debe estar al principio de una tabla o dentro de una fila de la tabla, y el número de celdas solo puede cambiar en uno. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Este mensaje cambia los parámetros del número de filas especificado por el miembro **cRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , si la tabla tiene tantas filas consecutivas. Si **cRow** es menor que 0, el mensaje se recorre en iteración hasta el final de la tabla. Si el recuento de celdas nuevo difiere del número de celdas actual en + 1 o 1, inserta o elimina la celda en el índice especificado por el miembro **iCell** de **TABLEROWPARMS**. La fila de la tabla inicial se identifica mediante una posición de carácter. Esta posición se especifica mediante miembros **cpStartRow** con valores que son mayores o iguales que cero. La posición debe estar dentro de la fila de la tabla, pero no dentro de una tabla anidada, a menos que desee cambiar los parámetros de la tabla s. Si el miembro **cpStartRow** es 1, la selección actual proporciona la posición del carácter. Para ello, coloque la selección en cualquier lugar dentro de la fila de la tabla o seleccione la fila con el extremo activo de la selección al final de la fila de la tabla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETTABLEPARMS em**](em-gettableparms.md)
</dt> </dl>

 

 





