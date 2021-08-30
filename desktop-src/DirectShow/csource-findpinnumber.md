---
description: El método FindPinNumber recupera el número de un pin especificado en el filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Método CSource.FindPinNumber (Source.h)
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
ms.openlocfilehash: e8082cb19b275f8ebfebd0f2c9beda0eb9854699bf92f29e9d994ee4391e628f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084105"
---
# <a name="csourcefindpinnumber-method"></a>Método CSource.FindPinNumber

El `FindPinNumber` método recupera el número de un pin especificado en el filtro.

## <a name="syntax"></a>Sintaxis


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ipin* 
</dt> <dd>

Puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de pin o 1 si no se encuentra el pin en este filtro. El primer pin tiene el número cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




