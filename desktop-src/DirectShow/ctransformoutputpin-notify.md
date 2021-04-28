---
description: 'Método CTransformOutputPin.Notify: el método Notify notifica al pin que se solicita un cambio de calidad. Este método implementa el método IQualityControl::Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin.Notify (Transfrm.h)
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
ms.openlocfilehash: 9a55e493c737b5a5864ec0a8dd38eee3abbfa586
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084813"
---
# <a name="ctransformoutputpinnotify-method"></a>CTransformOutputPin.Notify (método)

El `Notify` método notifica al pin que se solicita un cambio de calidad. Este método implementa el [**método IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

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

Puntero a la [**interfaz IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.

</dd> <dt>

*Q* 
</dt> <dd>

[**Estructura**](/windows/win32/api/strmif/ns-strmif-quality) de calidad que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | No se encontró un objeto para aceptar el mensaje.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al método [**CTransformFilter::AlterQuality del**](ctransformfilter-alterquality.md) filtro. Si el filtro no controla el mensaje de calidad, este método llama al método [**CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md) en el pin de entrada del filtro. El **método PassNotify** pasa el mensaje de calidad ascendente (o a un administrador de calidad personalizado, si se instaló uno).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




