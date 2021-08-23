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
ms.openlocfilehash: 9544a5f35c42fcf65bff58ad63d6f22bdd4dd817ae91951b01ffe122bce50c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954024"
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

## <a name="remarks"></a>Comentarios

Use este método para llamar a [**IPin::EndOfStream en**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) cada pin de entrada de nivel inferior que recibe datos de este objeto. Si los pin de salida del filtro derivan de [**CBaseOutputPin,**](cbaseoutputpin.md)llame al método [**CBaseOutputPin::D eliverEndOfStream.**](cbaseoutputpin-deliverendofstream.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




