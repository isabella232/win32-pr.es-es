---
description: La \_ variable miembro m pAlloc es un puntero a la interfaz IMemAllocator del asignador de memoria.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Miembro CPullPin:: m_pAlloc (Pullpin. h)'
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
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671383"
---
# <a name="cpullpinm_palloc-member"></a>Miembro pAlloc CPullPin:: m \_

La `m_pAlloc` variable miembro es un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador de memoria.

## <a name="syntax"></a>Sintaxis


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Observaciones

El método [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) establece esta variable miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




