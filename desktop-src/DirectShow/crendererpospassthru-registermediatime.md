---
description: El método RegisterMediaTime almacena en caché las marcas de tiempo del ejemplo actual.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660452"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)

El método **RegisterMediaTime** almacena en caché las marcas de tiempo del ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                        |
| <dl> <dt>**\_tiempo medio de VFW E \_ \_ \_ no \_ establecido**</dt> </dl> | El ejemplo no tiene una marca de tiempo.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método almacena las marcas de tiempo del ejemplo actual. El método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera los mismos valores.

El filtro debe llamar a este método para cada ejemplo que recibe. El método se sobrecarga para aceptar un puntero al ejemplo o los propios valores de la marca de tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




