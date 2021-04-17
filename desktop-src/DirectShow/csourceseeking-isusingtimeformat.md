---
description: El método IsUsingTimeFormat determina si un formato de hora especificado es el formato que se está usando actualmente.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Método CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660776"
---
# <a name="csourceseekingisusingtimeformat-method"></a>CSourceSeeking. IsUsingTimeFormat, método

El `IsUsingTimeFormat` método determina si un formato de hora especificado es el formato que se está usando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsUsingTimeFormat(
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



| Código devuelto                                                                               | Descripción                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | El formato especificado no es el formato actual.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El formato especificado es el formato actual.<br/>     |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo** .<br/>                      |



 

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

 

 




