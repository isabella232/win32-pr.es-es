---
description: El método GetIDsOfNames asigna un conjunto de nombres a un conjunto correspondiente de DispId.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Método CMediaPosition. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681014"
---
# <a name="cmediapositiongetidsofnames-method"></a>CMediaPosition. GetIDsOfNames (método)

El `GetIDsOfNames` método asigna un conjunto de nombres a un conjunto correspondiente de DispId.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Reservado. Use IID \_ null.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Dirección de una matriz de cadenas de caracteres anchos que contienen los nombres que se van a asignar.

</dd> <dt>

*CNAME* 
</dt> <dd>

Tamaño de la matriz proporcionado por el parámetro *rgszNames* .

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se van a interpretar los nombres. Puede ser **null**.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntero a una matriz que recibe los DispId. Cada elemento de recibe un identificador que corresponde a uno de los nombres pasados en el parámetro *rgszNames* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                         | Descripción                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Correcto.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memoria insuficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | No se conocían uno o varios de los nombres.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




