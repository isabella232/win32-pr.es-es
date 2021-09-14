---
description: El método Allocator recupera un puntero al asignador de memoria.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Método CRendererInputPin.Allocator (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062392"
---
# <a name="crendererinputpinallocator-method"></a>Método CRendererInputPin.Allocator

El `Allocator` método recupera un puntero al asignador de memoria.

## <a name="syntax"></a>Sintaxis


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador o **NULL.**

## <a name="remarks"></a>Observaciones

Este método devuelve la variable [**miembro CBaseInputPin::m \_ pAllocator.**](cbaseinputpin-m-pallocator.md) El método no incrementa el recuento de referencias en la interfaz . Este método es estrictamente un método de accessor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 




