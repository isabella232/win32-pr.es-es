---
description: El método DeliverBeginFlush solicita la clavija de entrada conectada para iniciar una operación de vaciado.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Método CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661197"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>CBaseOutputPin. DeliverBeginFlush, método

El `DeliverBeginFlush` método solicita la clavija de entrada conectada para iniciar una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




