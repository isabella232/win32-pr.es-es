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
ms.openlocfilehash: 1bd8582d16022c9d5dfd60eb87847d564ef69203e329ff37eaa9c2964a11794c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317515"
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



 

## <a name="remarks"></a>Comentarios

Este método implementa el [**método IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) Para construir una cadena de identificador, el pin llama al [**método CSource::FindPinNumber**](csource-findpinnumber.md) con sí mismo como parámetro. El **método FindPinNumber** devuelve el número de pin, indexado a partir de cero. `QueryId` incrementa el valor devuelto en uno y convierte el resultado en una cadena. Por ejemplo, el primer pin se convierte en "1"; el segundo pin se convierte en "2"; y así sucesivamente.

Si este método devuelve VFW E NOT FOUND, indica que la matriz de pines del filtro no es \_ \_ válida, presumiblemente causada por un \_ error en el filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




