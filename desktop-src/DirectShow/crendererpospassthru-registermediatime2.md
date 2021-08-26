---
description: El método RegisterMediaTime almacena en caché las marcas de tiempo del ejemplo actual. Este método usa los *parámetros StartTime* *y EndTime.*
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: 'Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h): parámetros StartTime y EndTime'
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
ms.openlocfilehash: 944d78af6247e7237040f0260a51203a13ef506db36856cfb554d0f2982c0d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084115"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h): parámetros StartTime y EndTime

El [**método RegisterMediaTime**](crendererpospassthru-registermediatime.md) almacena en caché las marcas de tiempo del ejemplo actual.

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

Hora de inicio de ejemplo, en unidades de 100 nanosegundos.

</dd> <dt>

*EndTime* 
</dt> <dd>

Hora de finalización de la muestra, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Correcto.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método almacena los valores de marca de tiempo dados *en StartTime* y *EndTime.* El [**método CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) recupera los mismos valores.

El filtro debe llamar a este método para cada muestra que reciba. El método se sobrecarga para aceptar un puntero al ejemplo o los propios valores de marca de tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Ctlutil.h (incluir Secuencias.h)                                                                                   |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |



 

 




