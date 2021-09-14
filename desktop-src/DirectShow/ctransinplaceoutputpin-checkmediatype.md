---
description: 'Método CTransInPlaceOutputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Método CTransInPlaceOutputPin.CheckMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973819"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>Método CTransInPlaceOutputPin.CheckMediaType

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                 |
| <dl> <dt>**TIPO E VFW \_ \_ NO \_ \_ ACEPTADO**</dt> </dl> | Tipo de medio no aceptado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CTransformOutputPin::CheckMediaType.**](ctransformoutputpin-checkmediatype.md)

Si el filtro ya está transmitiendo y usa dos asignadores, este método rechaza los cambios de formato. De lo contrario, este método llama al método [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio. Si el pin de entrada está conectado, también llama al método [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin de salida ascendente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceOutputPin (clase)**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




