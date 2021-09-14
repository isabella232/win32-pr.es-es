---
description: Se llama al método EndOfStream después de que el objeto entregue el último ejemplo. La clase derivada debe implementar este método.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Método CPullPin.EndOfStream (Pullpin.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063312"
---
# <a name="cpullpinendofstream-method"></a>Método CPullPin.EndOfStream

Se `EndOfStream` llama al método después de que el objeto entregue el último ejemplo. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Use este método para llamar a [**IPin::EndOfStream en**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) cada pin de entrada de nivel inferior que recibe datos de este objeto. Si los pin de salida del filtro derivan de [**CBaseOutputPin,**](cbaseoutputpin.md)llame al método [**CBaseOutputPin::D eliverEndOfStream.**](cbaseoutputpin-deliverendofstream.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




