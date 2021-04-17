---
description: 'El método QueryPreferredFormat recupera el formato de hora preferido del objeto. Este método implementa el método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Método CSourceSeeking. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690467"
---
# <a name="csourceseekingquerypreferredformat-method"></a>CSourceSeeking. QueryPreferredFormat, método

El `QueryPreferredFormat` método recupera el formato de hora preferido del objeto. Este método implementa el método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a una variable que recibe un GUID con formato de hora. Consulte [**GUID de formato de hora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl> | Valor de puntero **nulo**<br/> |



 

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

 

 




