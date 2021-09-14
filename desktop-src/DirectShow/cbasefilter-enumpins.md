---
description: El método EnumPins enumera los pines de este filtro. Este método implementa el método IBaseFilter::EnumPins.
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Método CBaseFilter.EnumPins (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973999"
---
# <a name="cbasefilterenumpins-method"></a>Método CBaseFilter.EnumPins

El `EnumPins` método enumera los pines de este filtro. Este método implementa el [**método IBaseFilter::EnumPins.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la [**interfaz IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Observaciones

Este método crea una instancia de la clase base [**CEnumPins**](cenumpins.md) y devuelve un puntero a ese objeto, de tipo **IEnumPins**. La **clase CEnumPins** llama al método [**CBaseFilter::GetPin**](cbasefilter-getpin.md) del filtro para enumerar los pines del filtro.

Si este método se realiza correctamente, la **interfaz IEnumPins** tiene un recuento de referencias pendiente. El autor de la llamada debe liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




