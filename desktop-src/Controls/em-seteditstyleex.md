---
title: EM_SETEDITSTYLEEX mensaje (Richedit.h)
description: Establece las marcas de estilo de edición extendida actuales.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX controles de Windows mensaje
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
ms.openlocfilehash: 4b96a353b62dc3a31affd9e827ee803c481bcd806eaad9f8a5d0e9dd35388cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831226"
---
# <a name="em_seteditstyleex-message"></a>Mensaje \_ EM SETEDITSTYLEEX

Establece las marcas de estilo de edición extendida actuales.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica una o varias marcas de estilo de edición extendidas. Para obtener una lista de valores posibles, [**vea EM \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara que consta de uno o varios de los *valores wParam.* Solo se establecerán o borrarán los valores especificados en esta máscara. Esto permite establecer o borrar una sola marca sin leer los estados de marca actuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el estado de las marcas de estilo de edición extendidas después de que la edición enriquezca haya intentado implementar los cambios de estilo de edición. Las marcas de estilo de edición son un conjunto de marcas que indican el estilo de edición actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETEDITSTYLEEX**](em-geteditstyleex.md)
</dt> </dl>

 

