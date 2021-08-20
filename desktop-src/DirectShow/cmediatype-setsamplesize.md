---
description: El método SetSampleSize especifica un tamaño de muestra fijo o especifica que las muestras tienen un tamaño variable.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Método CMediaType.SetSampleSize (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a29393ed4c9251d1e12895ad57a61f96bdc80bb05757ce72fc9485bb42a1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954414"
---
# <a name="cmediatypesetsamplesize-method"></a>Método CMediaType.SetSampleSize

El `SetSampleSize` método especifica un tamaño de muestra fijo o especifica que las muestras tienen un tamaño variable.

## <a name="syntax"></a>Sintaxis


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Sz* 
</dt> <dd>

Tamaño de la muestra, en bytes o cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si el valor de *sz* es cero, el tipo de medio usa tamaños de ejemplo variables. De lo contrario, el tamaño de la muestra se fija en *bytes sz.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




