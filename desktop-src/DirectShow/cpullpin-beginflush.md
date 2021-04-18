---
description: El método BeginFlush informa al filtro propietario de vaciar los filtros de nivel inferior. La clase derivada debe implementar este método.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Método CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680276"
---
# <a name="cpullpinbeginflush-method"></a>CPullPin. BeginFlush, método

El `BeginFlush` método informa al filtro propietario de vaciar los filtros de nivel inferior. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

El método [**CPullPin:: Seek**](cpullpin-seek.md) llama a este método. Implemente este método para llamar al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en cada pin de entrada de nivel inferior que reciba datos de este objeto. Si los anclajes de salida del filtro se derivan de [**CBaseOutputPin**](cbaseoutputpin.md), llame al método [**eliverbeginflush de CBaseOutputPin::D**](cbaseoutputpin-deliverbeginflush.md) .

Este diseño permite que el filtro busque el flujo simplemente mediante una llamada a **Seek** en el objeto **CPullPin** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




