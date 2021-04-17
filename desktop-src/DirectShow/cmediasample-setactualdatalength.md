---
description: 'El método SetActualDataLength establece la longitud de los datos válidos en el búfer. Este método implementa el método IMediaSample:: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Método CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670531"
---
# <a name="cmediasamplesetactualdatalength-method"></a>CMediaSample. SetActualDataLength, método

El `SetActualDataLength` método establece la longitud de los datos válidos en el búfer. Este método implementa el método [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lLen* 
</dt> <dd>

Longitud de los datos válidos, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                             | Descripción                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                         |
| <dl> <dt>**desbordamiento de búfer de VFW \_ E \_ \_**</dt> </dl> | *lLen* es mayor que el tamaño de búfer asignado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método establece la variable miembro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




