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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973889"
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

## <a name="remarks"></a>Observaciones

Si *pEnumMediaTypes* es **NULL,** este método inicializa el enumerador al principio de la secuencia de enumeración. De lo contrario, duplica el estado interno del enumerador especificado por *pEnumMediaTypes*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CEnumMediaTypes (clase)**](cenummediatypes.md)
</dt> </dl>

 

 




