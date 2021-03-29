---
description: Se llama al método EndOfStream después de que el objeto entregue el último ejemplo. La clase derivada debe implementar este método.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Método CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680834"
---
# <a name="cpullpinendofstream-method"></a>CPullPin. EndOfStream, método

`EndOfStream`Se llama al método después de que el objeto entregue el último ejemplo. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Use este método para llamar a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en cada pin de entrada de nivel inferior que reciba datos de este objeto. Si los anclajes de salida del filtro se derivan de [**CBaseOutputPin**](cbaseoutputpin.md), llame al método [**eliverendofstream de CBaseOutputPin::D**](cbaseoutputpin-deliverendofstream.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




