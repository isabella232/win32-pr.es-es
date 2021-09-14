---
description: El método QueryId recupera un identificador para el pin.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Método CSourceStream.QueryId (Source.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362451"
---
# <a name="csourcestreamqueryid-method"></a>Método CSourceStream.QueryId

El `QueryId` método recupera un identificador para el pin.

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

Puntero a una variable que recibe una cadena que contiene el identificador de pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insuficiente.<br/>             |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>         | **Argumento de** puntero NULL.<br/>       |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | No se encontró el pin en el filtro.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método implementa el [**método IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) Para construir una cadena de identificador, el pin llama al [**método CSource::FindPinNumber**](csource-findpinnumber.md) con sí mismo como parámetro. El **método FindPinNumber** devuelve el número de pin, indexado a partir de cero. `QueryId` incrementa el valor devuelto en uno y convierte el resultado en una cadena. Por ejemplo, el primer pin se convierte en "1"; el segundo pin se convierte en "2"; etc.

Si este método devuelve VFW E NOT FOUND, indica que la matriz de pines del filtro no es \_ \_ válida, presumiblemente debido a un error en \_ el filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




