---
description: El método SetProperties establece las propiedades del ejemplo. Este método implementa el método IMediaSample2::SetProperties.
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Método CMediaSample.SetProperties (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4bac378d41e0a9933f0903990e6368979c669c048102665a06b2ce59e4a45c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156537"
---
# <a name="cmediasamplesetproperties-method"></a>Método CMediaSample.SetProperties

El `SetProperties` método establece las propiedades del ejemplo. Este método implementa el [**método IMediaSample2::SetProperties.**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cbProperties* 
</dt> <dd>

Longitud de los datos de propiedad que se establecerán, en bytes.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Puntero a un búfer de tamaño *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




