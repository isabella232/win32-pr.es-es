---
description: Puntero al asignador que creó este ejemplo.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Miembro CMediaSample:: m_pAllocator (Amfilter. h)'
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
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670463"
---
# <a name="cmediasamplem_pallocator-member"></a>Miembro pAllocator CMediaSample:: m \_

Puntero al asignador que creó este ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Observaciones

Aunque el ejemplo mantiene un puntero al asignador, no contiene un recuento de referencias. En su lugar, el asignador incrementa su propio recuento de referencias en el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) y se publica en el método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) . Esto garantiza que el asignador estará disponible siempre que otro objeto esté usando el ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




