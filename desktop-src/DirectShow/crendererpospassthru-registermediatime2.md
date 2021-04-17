---
description: El método RegisterMediaTime almacena en caché las marcas de tiempo del ejemplo actual. Este método usa los parámetros *startTime* y *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: 'Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h): parámetros StartTime y EndTime'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187830"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h): parámetros StartTime y EndTime

El método [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) almacena en caché las marcas de tiempo del ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartTime* 
</dt> <dd>

Hora de inicio de ejemplo, en unidades de 100-nanosegundos.

</dd> <dt>

*EndTime* 
</dt> <dd>

Hora de finalización del ejemplo, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Correcto.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método almacena los valores de marca de tiempo especificados en *startTime* y *EndTime*. El método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera los mismos valores.

El filtro debe llamar a este método para cada ejemplo que recibe. El método se sobrecarga para aceptar un puntero al ejemplo o los propios valores de la marca de tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Ctlutil. h (incluir streams. h)                                                                                   |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |



 

 




