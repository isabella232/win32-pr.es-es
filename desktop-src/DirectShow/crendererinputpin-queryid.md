---
description: 'El método QueryId recupera el identificador del PIN. Este método invalida el método CBasePin:: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Método CRendererInputPin. QueryId (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671701"
---
# <a name="crendererinputpinqueryid-method"></a>CRendererInputPin. QueryId (método)

El `QueryId` método recupera el identificador del PIN. Este método invalida el método [**CBasePin:: queryId**](cbasepin-queryid.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Recibe una cadena que contiene el identificador del PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>       |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

Este método asigna la cadena de caracteres anchos "in" y la asigna al parámetro *ID* . El llamador debe liberar la memoria asignada mediante la función **CoTaskMemFree** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




