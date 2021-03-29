---
description: 'El método QueryId recupera un identificador para el código PIN. Este método implementa el método IPin:: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Método CTransformOutputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680741"
---
# <a name="ctransformoutputpinqueryid-method"></a>CTransformOutputPin. QueryId (método)

El `QueryId` método recupera un identificador para el código PIN. Este método implementa el método [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

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

El identificador del PIN se usa para la persistencia del gráfico. El identificador de PIN de esta clase está fuera. Esta clase invalida el comportamiento de la clase [**CBasePin**](cbasepin.md) . En la clase **CBasePin** , el identificador del PIN es el mismo que el nombre del PIN especificado en el constructor de clase. En la clase **CTransformInputPin** , el identificador del PIN y el nombre del PIN no son los mismos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




