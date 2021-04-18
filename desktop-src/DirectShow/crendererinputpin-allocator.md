---
description: El método allocator recupera un puntero al asignador de memoria.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Método CRendererInputPin. allocator (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670983"
---
# <a name="crendererinputpinallocator-method"></a>CRendererInputPin. allocator (método)

El `Allocator` método recupera un puntero al asignador de memoria.

## <a name="syntax"></a>Sintaxis


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador o **null**.

## <a name="remarks"></a>Observaciones

Este método devuelve la variable miembro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) . El método no incrementa el recuento de referencias en la interfaz. Este método es estrictamente un método de descriptor de acceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




