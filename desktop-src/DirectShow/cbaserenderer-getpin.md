---
description: 'Método CBaseRenderer.GetPin: el método GetPin recupera un pin.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer.GetPin (Renbase.h)
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
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822706"
---
# <a name="cbaserenderergetpin-method"></a>Método CBaseRenderer.GetPin

El `GetPin` método recupera un pin.

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

Número del pin especificado. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**puntero CBaseRenderer::m \_ pInputPin.**](cbaserenderer-m-pinputpin.md)

## <a name="remarks"></a>Comentarios

Este método implementa el [**método CBaseFilter::GetPin,**](cbasefilter-getpin.md) que es virtual puro en la **clase CBaseFilter.** El filtro admite exactamente un pin (el pin de entrada). La primera vez que se llama a este método, crea el pin como un nuevo [**objeto CRendererInputPin.**](crendererinputpin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




