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
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061330"
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

## <a name="remarks"></a>Observaciones

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

 

 




