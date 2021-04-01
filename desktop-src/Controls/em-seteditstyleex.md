---
title: Mensaje EM_SETEDITSTYLEEX (RichEdit. h)
description: Establece las marcas de estilo de edición extendida actual.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996927"
---
# <a name="em_seteditstyleex-message"></a>\_Mensaje SETEDITSTYLEEX em

Establece las marcas de estilo de edición extendida actual.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica una o más marcas de estilo de edición extendida. Para obtener una lista de los valores posibles, vea [**em \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara formada por uno o varios de los valores de *wParam* . Solo se establecerán o se borrarán los valores especificados en esta máscara. Esto permite establecer o borrar una sola marca sin leer los Estados actuales de la marca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el estado de las marcas de estilo de edición extendidas después de que la edición enriquecida haya intentado implementar los cambios de estilo de edición. Las marcas de estilo de edición son un conjunto de marcas que indican el estilo de edición actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETEDITSTYLEEX em**](em-geteditstyleex.md)
</dt> </dl>

 

