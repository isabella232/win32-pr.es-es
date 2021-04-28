---
description: 'Método CTransformInputPin.EndFlush: el método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin::EndFlush.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Método CTransformInputPin.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095063"
---
# <a name="ctransforminputpinendflush-method"></a>Método CTransformInputPin.EndFlush

El `EndFlush` método finaliza una operación de vaciado. Este método implementa el [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin de salida no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al método [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) del filtro para entregar la llamada de nivel inferior. A continuación, llama al método [**CBaseInputPin::EndFlush del**](cbaseinputpin-endflush.md) pin.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




