---
description: El método AddPin agrega un nuevo PIN de salida al filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: CSource. AddPin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670400"
---
# <a name="csourceaddpin-method"></a>CSource. AddPin, método

El `AddPin` método agrega un nuevo PIN de salida al filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStream* 
</dt> <dd>

Puntero al objeto [**CSourceStream**](csourcestream.md) que implementa el código PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando se crea un nuevo PIN derivado de **CSourceStream**, el constructor **CSourceStream** llama automáticamente a este método para agregar el PIN de salida al filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSource**](csource.md)
</dt> </dl>

 

 




