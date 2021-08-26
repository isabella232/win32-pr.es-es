---
description: El método CBaseInputPin comienza una operación de vaciado. Este método implementa el método IPin::BeginFlush.
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Método CBaseInputPin.BeginFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b9e5e4e97a3a010523f61cc9efedf224d8dfc7fa373c9514b6d38dc0105d2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103215"
---
# <a name="cbaseinputpinbeginflush-method"></a>Método CBaseInputPin.BeginFlush

El `CBaseInputPin` método comienza una operación de vaciado. Este método implementa el [**método IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método establece la marca [**CBaseInputPin::m \_ bFlushing**](cbaseinputpin-m-bflushing.md) en **TRUE,** lo que hace que el método [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) rechace más ejemplos.

La clase derivada debe invalidar este método y realizar los pasos siguientes:

1.  Llame al [**método IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en los pines de entrada de bajada. Si el pin aún no ha entregado ningún ejemplo multimedia de nivel inferior, puede omitir este paso. Si los pines de salida derivan de la clase [**CBaseOutputPin,**](cbaseoutputpin.md) puede llamar al método [**CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)
2.  Llame al método de clase base.
3.  Comience a descartar los datos en cola.
4.  Devuelve de las llamadas bloqueadas al **método Receive.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




