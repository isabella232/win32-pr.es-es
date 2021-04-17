---
description: El \_ método get FramesDroppedInRenderer recupera el número de fotogramas quitados por el representador.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Método CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660380"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>CBaseVideoRenderer. Get \_ FramesDroppedInRenderer (método)

El `get_FramesDroppedInRenderer` método recupera el número de fotogramas quitados por el representador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcFramesDropped* 
</dt> <dd>

Puntero al número de fotogramas quitados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IQualProp:: get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . Así es como la página de propiedades recupera los datos del programador. Los fotogramas también se pueden quitar de nivel superior sin que el representador los vea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




