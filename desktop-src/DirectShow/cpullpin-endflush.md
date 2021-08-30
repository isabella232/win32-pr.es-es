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
ms.openlocfilehash: e5102478807b49c796b06669979e528e8b2d79cd11bd1a5fc158e766b3f081e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055055"
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

## <a name="remarks"></a>Comentarios

El [**método CPullPin::Seek**](cpullpin-seek.md) llama a este método. Implemente este método para llamar al [**método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en cada pin de entrada de nivel inferior que recibe datos de este objeto. Si los pin de salida del filtro derivan de **CBaseOutputPin,** llame al método **CBaseOutputPin::D eliverEndFlush.**

Este diseño permite que el filtro busque la secuencia simplemente llamando a **Seek** en el **objeto CPullPin.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




