---
description: El método GetProperties recupera las propiedades del ejemplo. Este método implementa el método IMediaSample2::GetProperties.
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Método CMediaSample.GetProperties (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 856da0c73f3dd93d0c660f55aa0a9de35d87ab1b270df2179d7ad0b520e6d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074029"
---
# <a name="cmediasamplegetproperties-method"></a>Método CMediaSample.GetProperties

El `GetProperties` método recupera las propiedades del ejemplo. Este método implementa el [**método IMediaSample2::GetProperties.**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cbProperties* 
</dt> <dd>

Longitud de los datos de propiedad que se recuperarán, en bytes.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Puntero a un búfer de tamaño *cbProperties.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | Argumento de puntero **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




