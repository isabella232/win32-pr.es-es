---
description: El método FindPinNumber recupera el número de un PIN especificado en el filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: CSource. FindPinNumber (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689997"
---
# <a name="csourcefindpinnumber-method"></a>CSource. FindPinNumber, método

El `FindPinNumber` método recupera el número de un PIN especificado en el filtro.

## <a name="syntax"></a>Sintaxis


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de PIN o 1 si no se encuentra el PIN en este filtro. El primer pin tiene el número cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSource**](csource.md)
</dt> </dl>

 

 




