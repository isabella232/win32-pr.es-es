---
description: La \_ variable miembro m pAlloc es un puntero a la interfaz IMemAllocator del asignador de memoria.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: CPullPin::m_pAlloc miembro (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76abcdadf24006d545a8e8cf51205a99656a634094487104b9bad5d9b553c33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073459"
---
# <a name="cpullpinm_palloc-member"></a>CPullPin::m \_ miembro pAlloc

La `m_pAlloc` variable miembro es un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador de memoria.

## <a name="syntax"></a>Sintaxis


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Comentarios

El [**método CPullPin::D ecideAllocator**](cpullpin-decideallocator.md) establece esta variable miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




