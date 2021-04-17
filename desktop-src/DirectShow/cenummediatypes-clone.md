---
description: 'El método Clone realiza una copia del enumerador con el mismo estado de enumeración. Este método implementa el método IEnumMediaTypes:: Clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Método CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671161"
---
# <a name="cenummediatypesclone-method"></a>CEnumMediaTypes. Clone (método)

El `Clone` método realiza una copia del enumerador con el mismo estado de enumeración. Este método implementa el método [**IEnumMediaTypes:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) del nuevo enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto.<br/>                                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Memoria insuficiente.<br/>                                                     |
| <dl> <dt>**\_puntero E**</dt> </dl>                  | Argumento de puntero **nulo** .<br/>                                               |
| <dl> <dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt> </dl> | El estado del PIN ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




