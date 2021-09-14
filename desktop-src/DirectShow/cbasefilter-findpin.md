---
description: 'Método CBaseFilter.FindPin: el método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter::FindPin.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Método CBaseFilter.FindPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973998"
---
# <a name="cbasefilterfindpin-method"></a>Método CBaseFilter.FindPin

El `FindPin` método recupera el pin con el identificador especificado. Este método implementa el método [**IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Puntero a una cadena Unicode constante terminada en NULL que identifica el pin.

</dd> <dt>

*ppPin* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                       | Descripción                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>         | **Argumento de** puntero NULL.<br/>     |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | No se encontró un pin correspondiente.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al [**método CBasePin::Name**](cbasepin-name.md) para comparar el nombre de cada pin con la cadena especificada por el *parámetro Id.*

Si el método se realiza correctamente, la **interfaz IPin** tiene un recuento de referencias pendiente. Asegúrese de liberarla cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




