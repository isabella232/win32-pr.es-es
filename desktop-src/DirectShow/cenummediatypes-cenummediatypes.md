---
description: Método de constructor.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Constructor CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
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
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660869"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Constructor CEnumMediaTypes. CEnumMediaTypes

Método de constructor.

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

Puntero a la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) de un enumerador que se va a clonar o **null**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si *pEnumMediaTypes* es **null**, este método inicializa el enumerador al principio de la secuencia de enumeración. De lo contrario, duplica el estado interno del enumerador especificado por *pEnumMediaTypes*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




