---
description: El método QueryId recupera un identificador para el código PIN.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: CSourceStream. QueryId (método, source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680689"
---
# <a name="csourcestreamqueryid-method"></a>CSourceStream. QueryId (método)

El `QueryId` método recupera un identificador para el código PIN.

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

Puntero a una variable que recibe una cadena que contiene el identificador del PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insuficiente.<br/>             |
| <dl> <dt>**\_puntero E**</dt> </dl>         | Argumento de puntero **nulo** .<br/>       |
| <dl> <dt>**VFW \_ E \_ no \_ encontrado**</dt> </dl> | No se encontró el PIN en el filtro.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método implementa el método [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) . Para construir una cadena de identificador, el PIN llama al método [**CSource:: FindPinNumber**](csource-findpinnumber.md) con sí mismo como parámetro. El método **FindPinNumber** devuelve el número PIN, indizado desde cero. `QueryId` incrementa el valor devuelto en uno y convierte el resultado en una cadena. Por ejemplo, el primer PIN se convierte en "1"; el segundo PIN se convierte en "2"; etc.

Si este método devuelve VFW \_ E \_ no \_ encontrado, indica que la matriz de PIN del filtro no es válida, supuestamente causada por un error en el filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




