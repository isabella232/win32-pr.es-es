---
description: El método BeginFlush informa al filtro propietario para vaciar los filtros de nivel inferior. La clase derivada debe implementar este método.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Método CPullPin.BeginFlush (Pullpin.h)
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
ms.openlocfilehash: d2c7998c1c38a533d67edcd2cc237188a627ec8258a8b0349066e31ecf0fbaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687755"
---
# <a name="cpullpinbeginflush-method"></a>Método CPullPin.BeginFlush

El `BeginFlush` método informa al filtro propietario para vaciar los filtros de nivel inferior. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

El [**método CPullPin::Seek**](cpullpin-seek.md) llama a este método. Implemente este método para llamar al método [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en cada pin de entrada de nivel inferior que recibe datos de este objeto. Si los pin de salida del filtro derivan de [**CBaseOutputPin,**](cbaseoutputpin.md)llame al método [**CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)

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

 

 




