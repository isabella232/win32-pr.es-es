---
description: 'Método CMediaPosition.GetIDsOfNames: el método GetIDsOfNames asigna un conjunto de nombres a un conjunto correspondiente de DISPIDs.'
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Método CMediaPosition.GetIDsOfNames (Ctlutil.h)
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
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095533"
---
# <a name="cmediapositiongetidsofnames-method"></a>Método CMediaPosition.GetIDsOfNames

El `GetIDsOfNames` método asigna un conjunto de nombres a un conjunto correspondiente de DISPID.

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

Reservado. Use IID \_ NULL.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Dirección de una matriz de cadenas de caracteres anchos que contienen los nombres que se asignarán.

</dd> <dt>

*cNames* 
</dt> <dd>

Tamaño de la matriz especificada por el *parámetro rgszNames.*

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretarán los nombres. Puede ser **NULL.**

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntero a una matriz que recibe los DISPID. Cada elemento de recibe un identificador que corresponde a uno de los nombres pasados en el *parámetro rgszNames.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                         | Descripción                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Correcto.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memoria insuficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | No se conocían uno o varios de los nombres.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 




