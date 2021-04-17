---
description: 'El método siguiente recupera un número especificado de PIN en la secuencia de enumeración. Este método implementa el método IEnumPins:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Método CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671154"
---
# <a name="cenumpinsnext-method"></a>CEnumPins. Next (método)

El método siguiente recupera un número especificado de PIN en la secuencia de enumeración. Este método implementa el método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cPins* 
</dt> <dd>

Número de clavijas que se van a recuperar.

</dd> <dt>

*ppPins* 
</dt> <dd>

Matriz de tamaño *cPins* que se rellena con punteros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntero a una variable que recibe el número de PIN recuperados. Puede ser **null** si *cPins* es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | No recuperó tantos PIN como se solicitó.<br/>                                 |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento no válido.<br/>                                                           |
| <dl> <dt>**\_puntero E**</dt> </dl>                  | Argumento de puntero **nulo** .<br/>                                                  |
| <dl> <dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt> </dl> | El estado del filtro ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método recupera punteros al número especificado de anclajes, empezando en la posición actual de la enumeración, y los coloca en la matriz especificada.

Este método llama al método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro para recuperar los pin.

Si el método se ejecuta correctamente, todos los punteros de **IPin** tienen recuentos de referencias pendientes. Asegúrese de liberarlos cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




