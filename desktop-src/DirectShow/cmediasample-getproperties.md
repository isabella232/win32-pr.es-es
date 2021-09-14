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
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254445"
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

Puntero a un búfer de tamaño *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




