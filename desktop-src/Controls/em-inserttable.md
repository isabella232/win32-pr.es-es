---
title: EM_INSERTTABLE mensaje (Richedit.h)
description: Inserta una o varias filas de tabla idénticas con celdas vacías.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE controles de Windows mensaje
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
ms.openlocfilehash: 5a015ae2b9a886ddfa24591944f3f70eca8cb192af771c821df9e4a403c837d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413063"
---
# <a name="em_inserttable-message"></a>Mensaje DE EM \_ INSERTTABLE

Inserta una o varias filas de tabla idénticas con celdas vacías.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
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

Devuelve S \_ OK si se inserta la tabla o un código de error si no es así.

## <a name="remarks"></a>Comentarios

Si el miembro **cpStartRow** de [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) es 1, este mensaje elimina el texto seleccionado (si existe) y, a continuación, inserta filas de tabla vacías con los parámetros de fila y celda especificados por *wParam* *y lParam.* Deja la selección que apunta al inicio de la primera celda de la primera fila. A continuación, el cliente puede rellenar las celdas de la tabla señalando la selección (o [**un ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) a las distintas marcas de fin de celda e insertando y formateando el texto deseado. Este texto puede incluir filas de tabla anidadas. Como alternativa, si el miembro **cpStartRow** de **TABLEROWPARMS** es 0 o superior, las filas de la tabla se insertan en la posición de carácter dada por **cpStartRow**. Esto solo cambia la selección actual si la tabla se inserta dentro del texto seleccionado.

Una tabla De edición enriqueceda de Microsoft consta de una secuencia de filas de tabla que, a su vez, constan de secuencias de párrafos. Una fila de tabla comienza con el párrafo especial del delimitador de dos caracteres U+FFF9 U+000D y termina con el párrafo del delimitador de dos caracteres U+FFFB U+000D. La marca de celda U+0007 finaliza cada celda, que se trata como una marca de fin de párrafo de forma dura igual que U+000D (CR). Los parámetros de fila y celda de la tabla se tratan como formato de párrafo especial de los delimitadores de fila de tabla. El formato contiene la información de la [**estructura TABLEROWPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) Los parámetros de celda que ofrece la [**estructura TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) se almacenan en una versión expandida de la matriz tabs. Este formato permite anidar tablas dentro de otras tablas, hasta quince niveles de profundidad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ INSERTIMAGE**](em-insertimage.md)
</dt> </dl>

 

 





