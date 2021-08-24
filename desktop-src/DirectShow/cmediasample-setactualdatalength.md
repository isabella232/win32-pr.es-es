---
description: El método SetActualDataLength establece la longitud de los datos válidos en el búfer. Este método implementa el método IMediaSample::SetActualDataLength.
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Método CMediaSample.SetActualDataLength (Amfilter.h)
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
ms.openlocfilehash: db090ad96f6c53f725aef7864e729b8083bfd1a02b30f0d699d30b5c6f8f71aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634385"
---
# <a name="cmediasamplesetactualdatalength-method"></a>CMediaSample.SetActualDataLength (método)

El `SetActualDataLength` método establece la longitud de los datos válidos en el búfer. Este método implementa el [**método IMediaSample::SetActualDataLength.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength)

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

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                             | Descripción                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                         |
| <dl> <dt>**VFW \_ E \_ BUFFER \_ OVERFLOW**</dt> </dl> | *lLen* es mayor que el tamaño de búfer asignado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método establece la [**variable miembro CMediaSample::m \_ lActual.**](cmediasample-m-lactual.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




