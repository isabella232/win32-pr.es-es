---
description: El método FindPin recupera el pin con el identificador especificado.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Método CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671071"
---
# <a name="cbaserendererfindpin-method"></a>CBaseRenderer. FindPin, método

El `FindPin` método recupera el pin con el identificador especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Puntero a una constante con una cadena de caracteres anchos terminada en null que identifica el PIN. Debe ser L "in".

</dd> <dt>

*ppPin* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN. Si se produce un error en el método, *\* ppPin* se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>         | Argumento de puntero **nulo** .<br/> |
| <dl> <dt>**VFW \_ E \_ no \_ encontrado**</dt> </dl> | Not found.<br/>                 |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseFilter:: FindPin**](cbasefilter-findpin.md) . El PIN del filtro solo (el PIN de entrada) se denomina "in".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




