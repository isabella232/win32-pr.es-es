---
description: 'Método CBaseMediaFilter.StreamTime: el método StreamTime recupera el tiempo de secuencia actual.'
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Método CBaseMediaFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273223"
---
# <a name="cbasemediafilterstreamtime-method"></a>Método CBaseMediaFilter.StreamTime

El `StreamTime` método recupera el tiempo de secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Referencia a un [**objeto CRefTime**](creftime.md) que recibe el tiempo de secuencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                      | Descripción                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Correcto.<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | No hay ningún reloj de referencia disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

La hora de la secuencia se define como la hora de referencia actual (según lo indicado por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseMediaFilter::m \_ tStart).**](cbasemediafilter-m-tstart.md) La marca de tiempo de un ejemplo multimedia especifica el tiempo de secuencia en el que se debe representar. Si aún no se ha representado un ejemplo con una marca de tiempo inferior a la hora de transmisión actual, es tarde.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 




