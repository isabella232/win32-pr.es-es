---
description: Método constructor. El constructor obtiene acceso al pin especificado.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Constructor CAutoUsingOutputPin.CAutoUsingOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0594eed7f253f7e540f843dfc3c3de6481d7dbede3f25d1534e52181ef0585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057525"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Constructor CAutoUsingOutputPin.CAutoUsingOutputPin

Método constructor. El constructor obtiene acceso al pin especificado.

## <a name="syntax"></a>Sintaxis


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Puntero a un [**objeto CDynamicOutputPin.**](cdynamicoutputpin.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que contiene un **valor HRESULT.** El valor debe ser S \_ OK.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando el método vuelve, el valor de *\* phr* indica el éxito o error del método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CAutoUsingOutputPin (clase)**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




