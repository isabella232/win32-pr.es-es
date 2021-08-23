---
description: El método CheckMediaType determina si el pin acepta un tipo de medio específico. Este método invalida el método CBasePin::CheckMediaType.
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Método CRendererInputPin.CheckMediaType (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d47f69c72ab2dab366b42d6dc80100508c0b1608d25abdcbfb1bb49c4177a278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687705"
---
# <a name="crendererinputpincheckmediatype-method"></a>Método CRendererInputPin.CheckMediaType

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico. Este método invalida el [**método CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a un objeto de tipo de medio que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 




