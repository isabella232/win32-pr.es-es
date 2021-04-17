---
description: 'El método IsFormatSupported determina si se admite un formato de hora especificado. Este método implementa el método IMediaSeeking:: IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Método CSourceSeeking. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690553"
---
# <a name="csourceseekingisformatsupported-method"></a>CSourceSeeking. IsFormatSupported, método

El `IsFormatSupported` método determina si se admite un formato de hora especificado. Este método implementa el método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a un GUID de formato de hora. Consulte [**GUID de formato de hora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | No se admite el formato.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Se admite el formato.<br/>     |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo** .<br/>   |



 

## <a name="remarks"></a>Observaciones

El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




