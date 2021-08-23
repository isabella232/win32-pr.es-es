---
description: El método SetDiscontinuity especifica si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el método IMediaSample::SetDiscontinuity.
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Método CMediaSample.SetDiscontinuity (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4189498c60a52692c057a867dba8bc48c43d2b1c32fbd6091738a3711102f4b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832185"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>Método CMediaSample.SetDiscontinuity

El `SetDiscontinuity` método especifica si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el [**método IMediaSample::SetDiscontinuity.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bDiscont* 
</dt> <dd>

Valor booleano que especifica si este ejemplo es una discontinuidad. Si **es TRUE,** el ejemplo multimedia es discontinuo con el ejemplo anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método actualiza la variable [**miembro CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica la propiedad discontinuity.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




