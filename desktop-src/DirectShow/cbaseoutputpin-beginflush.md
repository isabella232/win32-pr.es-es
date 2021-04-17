---
description: 'El método BeginFlush inicia una operación de vaciado. Implementa el método IPin:: BeginFlush.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Método CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671110"
---
# <a name="cbaseoutputpinbeginflush-method"></a>CBaseOutputPin. BeginFlush, método

El `BeginFlush` método inicia una operación de vaciado. Implementa el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ inesperado.

## <a name="remarks"></a>Observaciones

Solo se debe llamar a este método en los pin de entrada, por lo que la implementación de **CBaseOutputPin** devuelve E \_ inesperada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




