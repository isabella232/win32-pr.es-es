---
description: 'Constructor CEnumMediaTypes.CEnumMediaTypes: método constructor.'
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Constructor CEnumMediaTypes.CEnumMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189073bbf1f9c3f2d6475ecacacdbae7c7e7725bad392f726b9ee6faf0de3763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131305"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Constructor CEnumMediaTypes.CEnumMediaTypes

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero al pin en el que se va a realizar la enumeración.

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

Puntero a la [**interfaz IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) de un enumerador que se clona, o **NULL.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si *pEnumMediaTypes* es **NULL,** este método inicializa el enumerador al principio de la secuencia de enumeración. De lo contrario, duplica el estado interno del enumerador especificado por *pEnumMediaTypes*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CEnumMediaTypes (clase)**](cenummediatypes.md)
</dt> </dl>

 

 




