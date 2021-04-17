---
description: El \_ método get AvgFrameRate calcula y recupera la velocidad media de fotogramas obtenida.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Método CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661066"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>CBaseVideoRenderer. Get \_ AvgFrameRate (método)

El `get_AvgFrameRate` método calcula y recupera la velocidad media de fotogramas obtenida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

Puntero al número de fotogramas por segundo desde que comenzó la transmisión por secuencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IQualProp:: get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




