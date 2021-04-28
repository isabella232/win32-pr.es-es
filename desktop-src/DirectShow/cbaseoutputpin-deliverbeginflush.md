---
description: 'Método CBaseOutputPin.DeliverBeginFlush: el método DeliverBeginFlush solicita el pin de entrada conectado para iniciar una operación de vaciado.'
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Método CBaseOutputPin.DeliverBeginFlush (Amfilter.h)
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
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099523"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>Método CBaseOutputPin.DeliverBeginFlush

El `DeliverBeginFlush` método solicita el pin de entrada conectado para iniciar una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al [**método IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




