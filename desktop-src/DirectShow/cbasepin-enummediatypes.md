---
description: 'Método CBasePin.EnumMediaTypes: el método EnumMediaTypes enumera los tipos de medios preferidos del pin. Este método implementa el método IPin::EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Método CBasePin.EnumMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061350"
---
# <a name="cbasepinenummediatypes-method"></a>Método CBasePin.EnumMediaTypes

El `EnumMediaTypes` método enumera los tipos de medios preferidos del pin. Este método implementa el [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la [**interfaz IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                   | Descripción                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL.<br/> |



 

## <a name="remarks"></a>Observaciones

Los pines de entrada no son necesarios para enumerar los tipos preferidos. Los pines de salida deben enumerar al menos un tipo preferido. De lo contrario, ambos pines podrían carecer de un tipo preferido, lo que imposibilitó una conexión.

La **interfaz IEnumMediaTypes** funciona como un enumerador COM estándar. Para obtener más información, [vea Enumerar objetos en un filtro Graph](enumerating-objects-in-a-filter-graph.md). Si el método se realiza correctamente, la **interfaz IEnumMediaTypes** tiene un recuento de referencias pendiente. Asegúrese de liberarla cuando haya terminado.

La clase base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**. Llama al método [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin para enumerar los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




