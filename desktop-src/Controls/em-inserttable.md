---
title: Mensaje EM_INSERTTABLE (RichEdit. h)
description: Inserta una o varias filas de tabla idénticas con celdas vacías.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489448"
---
# <a name="em_inserttable-message"></a>\_Mensaje INSERTTABLE em

Inserta una o varias filas de tabla idénticas con celdas vacías.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
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

Devuelve S \_ OK si se inserta la tabla o un código de error si no lo está.

## <a name="remarks"></a>Observaciones

Si el miembro **cpStartRow** de [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) es 1, este mensaje elimina el texto seleccionado (si existe) y, a continuación, inserta filas de tabla vacías con los parámetros de fila y celda proporcionados por *wParam* e *lParam*. Deja la selección que apunta al principio de la primera celda de la primera fila. A continuación, el cliente puede rellenar las celdas de la tabla seleccionando la selección (o un [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) a las distintas marcas de final de celda e insertando y dando formato al texto deseado. Dicho texto puede incluir filas de tabla anidada. Como alternativa, si el miembro **cpStartRow** de **TABLEROWPARMS** es 0 o superior, las filas de la tabla se insertan en la posición de carácter proporcionada por **cpStartRow**. Esto solo cambia la selección actual si la tabla se inserta dentro del texto seleccionado.

Una tabla de edición enriquecida de Microsoft está formada por una secuencia de filas de la tabla que, a su vez, constan de secuencias de párrafos. Una fila de tabla comienza con el párrafo especial de delimitador de dos caracteres U + FFF9 U + 000D y termina con el párrafo de delimitador de dos caracteres U + FFFB U + 000D. Cada celda se termina con la marca de celda U + 0007, que se trata como una marca de final de párrafo de forma rígida como U + 000D (CR). Los parámetros de celda y fila de la tabla se tratan como un formato de párrafo especial de los delimitadores de fila de tabla. El formato contiene la información de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) . Los parámetros de celda proporcionados por la estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) se almacenan en una versión expandida de la matriz Tabs. Este formato permite anidar tablas dentro de otras tablas, hasta quince niveles de profundidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_INSERTIMAGE em**](em-insertimage.md)
</dt> </dl>

 

 





