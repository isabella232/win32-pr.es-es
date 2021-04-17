---
description: El método GetMediaType recupera un tipo de medio preferido.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: CSourceStream. GetMediaType (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62d79faab8d48d748f4a2c787dd1cbc8f6d2ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690597"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>CSourceStream. GetMediaType (método) (Source. h)

El `GetMediaType` método recupera un tipo de medio preferido.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                            | Descripción                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>              |
| <dl> <dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt> </dl> | Índice fuera del intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice inferior a cero.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>           | error inesperado.<br/>     |



 

## <a name="remarks"></a>Observaciones

Hay dos versiones de este método. Una versión invalida el método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) y toma un valor de índice como parámetro. La otra versión está diseñada para recuperar un tipo de medio único, por lo que carece del parámetro de índice.

El método de un solo parámetro devuelve E \_ inesperado. El método de dos parámetros comprueba que el parámetro *iPosition* es cero y, a continuación, llama a la versión de un solo parámetro. En función del número de tipos de medios que admita el PIN, debe invalidar uno de estos métodos:

-   Si el PIN admite exactamente un tipo de medio, invalide la versión de un solo parámetro. Rellene el tipo de medio que admite el PIN.
-   Si el PIN admite más de un tipo de medio, invalide la versión de dos parámetros. También invalide el método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




