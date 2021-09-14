---
description: El método EndFlush informa al filtro propietario para finalizar una operación de vaciado. La clase derivada debe implementar este método.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Método CPullPin.EndFlush (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063313"
---
# <a name="cpullpinendflush-method"></a>Método CPullPin.EndFlush

El `EndFlush` método informa al filtro propietario para finalizar una operación de vaciado. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

El [**método CPullPin::Seek**](cpullpin-seek.md) llama a este método. Implemente este método para llamar al método [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en cada pin de entrada de nivel inferior que recibe datos de este objeto. Si los pines de salida del filtro derivan de **CBaseOutputPin,** llame al método **CBaseOutputPin::D eliverEndFlush.**

Este diseño permite que el filtro busque la secuencia simplemente llamando a **Seek** en el **objeto CPullPin.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




