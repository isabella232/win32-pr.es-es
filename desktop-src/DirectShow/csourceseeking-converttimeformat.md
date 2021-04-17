---
description: 'El método ConvertTimeFormat convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Método CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690132"
---
# <a name="csourceseekingconverttimeformat-method"></a>CSourceSeeking. ConvertTimeFormat, método

El `ConvertTimeFormat` método convierte de un formato de hora a otro. Este método implementa el método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTarget* 
</dt> <dd>

Puntero a una variable que recibe la hora convertida.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Puntero al GUID del formato de destino. Si es **null**, se usa el formato actual. Consulte [**GUID de formato de hora**](time-format-guids.md).

</dd> <dt>

*Origen* 
</dt> <dd>

Valor de hora que se va a convertir.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Puntero al GUID del formato de hora del formato que se va a convertir. Si es **null**, se usa el formato actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido<br/>          |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos). Este método devuelve E \_ INVALIDARG, excepto en el caso trivial en el que *PTargetFormat* y *pSourceFormat* especifican el formato de hora de tiempo \_ \_ medio \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




