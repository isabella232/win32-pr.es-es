---
description: 'El método SKIP omite un número especificado de PIN en la secuencia de enumeración. Este método implementa el método IEnumPins:: SKIP.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: CEnumPins. SKIP (método) (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671153"
---
# <a name="cenumpinsskip-method"></a>CEnumPins. SKIP (método)

El `Skip` método omite un número especificado de PIN en la secuencia de enumeración. Este método implementa el método [**IEnumPins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cPins* 
</dt> <dd>

Número de clavijas que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Se omitió más allá del final de la secuencia.<br/>                                       |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto.<br/>                                                                    |
| <dl> <dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt> </dl> | El estado del filtro ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




