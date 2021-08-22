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
ms.openlocfilehash: 69cff051ecab1a93d9fdceac20143bef7d1959ff523aa5893e5ae9c633aa80f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538145"
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

[**Estructura de**](/windows/win32/api/strmif/ns-strmif-quality) calidad que contiene el mensaje de control de calidad.

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
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




