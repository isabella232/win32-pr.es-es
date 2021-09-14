---
description: El método InitializeOutputSample recupera un nuevo ejemplo de salida y lo inicializa.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: Método CTransformFilter.InitializeOutputSample (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246680"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>Método CTransformFilter.InitializeOutputSample

El `InitializeOutputSample` método recupera un nuevo ejemplo de salida y lo inicializa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de entrada.

</dd> <dt>

*ppOutSample* 
</dt> <dd>

Recibe un puntero a la interfaz **IMediaSample** del ejemplo de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Observaciones

El método [**CTransformFilter::Receive**](ctransformfilter-receive.md) llama a este método para preparar el ejemplo de salida. Por lo general, no tiene que llamar a este método en la clase derivada, a menos que invalide el **método Receive.**

Este método recupera un nuevo ejemplo del asignador del pin de salida. A continuación, copia las propiedades de ejemplo del ejemplo de entrada al ejemplo de salida. Las propiedades de ejemplo se definen en la [**estructura PROPIEDADES DE AM \_ SAMPLE2. \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




