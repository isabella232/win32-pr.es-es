---
description: Método de constructor. El constructor obtiene acceso al punto de conexión especificado.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Constructor CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661133"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Constructor CAutoUsingOutputPin. CAutoUsingOutputPin

Método de constructor. El constructor obtiene acceso al punto de conexión especificado.

## <a name="syntax"></a>Sintaxis


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Puntero a un objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que contiene un valor **HRESULT** . El valor debe ser S \_ OK.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando el método devuelve un resultado, el valor de *\* PHR* indica si el método se ha ejecutado correctamente o no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




