---
description: El \_ método get DevSyncOffset recupera la desviación estándar del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó en realidad, para todos los fotogramas desde que se inició el streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Método CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660382"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>CBaseVideoRenderer. Get \_ DevSyncOffset (método)

El `get_DevSyncOffset` método recupera la desviación estándar del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó en realidad, para todos los fotogramas desde que se inició el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piDev* 
</dt> <dd>

Puntero a la desviación estándar de la hora que se ha descrito anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IQualProp:: get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




