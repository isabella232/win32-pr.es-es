---
description: El método GetMediaType recupera un tipo de medio preferido.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: 'Método CSourceStream.GetMediaType (Source.h): parámetro pMediaType'
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
ms.openlocfilehash: 2850d08726337f1ff43ad09319aea8b0af95d107ad9dad9c0f89ce94474c7261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073199"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Método CSourceStream.GetMediaType (Source.h)

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                            | Descripción                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Índice fuera del intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que cero.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | error inesperado.<br/>     |



 

## <a name="remarks"></a>Comentarios

Hay dos versiones de este método. Una versión invalida el [**método CBasePin::GetMediaType**](cbasepin-getmediatype.md) y toma un valor de índice como parámetro. La otra versión está diseñada para recuperar un único tipo de medio, por lo que carece del parámetro index.

El método de parámetro único devuelve E \_ UNEXPECTED. El método de dos parámetros comprueba que el parámetro *iPosition* es cero y, a continuación, llama a la versión de parámetro único. En función del número de tipos de medios que admita el pin, debe invalidar uno de estos métodos:

-   Si el pin admite exactamente un tipo de medio, invalide la versión de parámetro único. Rellene el tipo de medio que admite el pin.
-   Si el pin admite más de un tipo de medio, invalide la versión de dos parámetros. Invalide también [**el método CSourceStream::CheckMediaType.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




