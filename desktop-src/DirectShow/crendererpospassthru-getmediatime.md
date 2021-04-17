---
description: El método GetMediaTime recupera las marcas de tiempo en el ejemplo actual.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Método CRendererPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671213"
---
# <a name="crendererpospassthrugetmediatime-method"></a>CRendererPosPassThru. GetMediaTime, método

El `GetMediaTime` método recupera las marcas de tiempo en el ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStartTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de inicio, en unidades del formato de hora actual.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de finalización, en unidades del formato de hora actual. Puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se admite la conversión a este formato.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/>                  |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) . Los valores de la marca de tiempo se convierten al formato de hora actual llamando al método [**CPosPassThru:: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




