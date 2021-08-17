---
description: Puntero al asignador que creó este ejemplo.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: CMediaSample::m_pAllocator miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 646c6fb7f8236aca87b5aebd1d30fd67750d960da4445d45bf45d8b601320274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156547"
---
# <a name="cmediasamplem_pallocator-member"></a>Miembro CMediaSample::m \_ pAllocator

Puntero al asignador que creó este ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Comentarios

Aunque el ejemplo mantiene un puntero al asignador, no contiene un recuento de referencias. En su lugar, el asignador incrementa su propio recuento de referencias en el método [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) y se libera en el método [**IMemAllocator::ReleaseBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) Esto garantiza que el asignador estará disponible siempre que otro objeto use el ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




