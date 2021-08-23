---
description: El método GetMediaType recupera un tipo de medio preferido. Este método usa los *parámetros iPosition* *y pMediaType.*
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: 'Método CSourceStream.GetMediaType (Source.h): parámetros iPosition y pMediaType'
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
ms.openlocfilehash: cb3095e366a03d94616d45eda441fec78d2ccbf7d58f8e74890a42902bae6fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073259"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>Método CSourceStream.GetMediaType (Source.h): parámetros iPosition y pMediaType

El **método GetMediaType** recupera un tipo de medio preferido.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice de base cero.

</dd> <dt>

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

El método de parámetro único devuelve E \_ UNEXPECTED. El método de dos parámetros comprueba que el parámetro *iPosition* es cero y, a continuación, llama a la versión de un solo parámetro. En función del número de tipos de medios que admita el pin, debe invalidar uno de estos métodos:

-   Si el pin admite exactamente un tipo de medio, invalide la versión de un solo parámetro. Rellene el tipo de medio que admite el pin.
-   Si el pin admite más de un tipo de medio, invalide la versión de dos parámetros. Invalide también [**el método CSourceStream::CheckMediaType.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Source.h (incluir Secuencias.h)                                                                                    |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




