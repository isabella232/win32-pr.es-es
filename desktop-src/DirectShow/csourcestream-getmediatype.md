---
description: El método GetMediaType recupera un tipo de medio preferido. Este método usa los parámetros *iPosition* y *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: 'CSourceStream. GetMediaType (método) (Source. h): parámetros iPosition y pMediaType'
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187942"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>CSourceStream. GetMediaType (método) (Source. h): parámetros iPosition y pMediaType

El método **GetMediaType** recupera un tipo de medio preferido.

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
| Encabezado  | Source. h (incluir streams. h)                                                                                    |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




