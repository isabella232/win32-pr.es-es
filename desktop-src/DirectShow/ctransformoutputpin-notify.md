---
description: 'El método Notify notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método IQualityControl:: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin. Notify (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661003"
---
# <a name="ctransformoutputpinnotify-method"></a>CTransformOutputPin. Notify (método)

El `Notify` método notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSelf* 
</dt> <dd>

Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.

</dd> <dt>

*respuestas* 
</dt> <dd>

Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ no \_ encontrado**</dt> </dl> | No se encontró un objeto para aceptar el mensaje.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) del filtro. Si el filtro no controla el mensaje de calidad, este método llama al método [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md) en el PIN de entrada del filtro. El método **PassNotify** pasa el mensaje de calidad ascendente (o a un administrador de calidad personalizado, si se ha instalado alguno).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




