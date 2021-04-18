---
description: El método GetPin recupera un PIN.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660284"
---
# <a name="cbaserenderergetpin-method"></a>CBaseRenderer. GetPin, método

El `GetPin` método recupera un PIN.

## <a name="syntax"></a>Sintaxis


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número del PIN especificado. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el puntero [**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md) .

## <a name="remarks"></a>Observaciones

Este método implementa el método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) , que es virtual puro en la clase **CBaseFilter** . El filtro admite exactamente un PIN (el PIN de entrada). La primera vez que se llama a este método, se crea el PIN como un nuevo objeto [**CRendererInputPin**](crendererinputpin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




