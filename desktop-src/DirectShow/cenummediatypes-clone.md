---
description: El método Clone realiza una copia del enumerador con el mismo estado de enumeración. Este método implementa el método IEnumMediaTypes::Clone.
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Método CEnumMediaTypes.Clone (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973886"
---
# <a name="cenummediatypesclone-method"></a>Método CEnumMediaTypes.Clone

El `Clone` método realiza una copia del enumerador con el mismo estado de enumeración. Este método implementa el [**método IEnumMediaTypes::Clone.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone)

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

Dirección de una variable que recibe un puntero a la [**interfaz IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) del nuevo enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Memoria insuficiente.<br/>                                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                  | **Argumento de** puntero NULL.<br/>                                               |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | El estado del pin ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CEnumMediaTypes (clase)**](cenummediatypes.md)
</dt> </dl>

 

 




