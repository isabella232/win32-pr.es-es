---
description: El método Skip omite un número especificado de tipos de medios. Este método implementa el método IEnumMediaTypes::Skip.
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Método CEnumMediaTypes.Skip (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973883"
---
# <a name="cenummediatypesskip-method"></a>CEnumMediaTypes.Skip (método)

El `Skip` método omite un número especificado de tipos de medios. Este método implementa el [**método IEnumMediaTypes::Skip.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Número de tipos de medios que se omitirán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Se omite más allá del final de la secuencia.<br/>                                    |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                                                                 |
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

 

 




