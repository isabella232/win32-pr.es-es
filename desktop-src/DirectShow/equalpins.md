---
description: La función EqualPins comprueba si dos patillas están en el mismo objeto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Función EqualPins (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690081"
---
# <a name="equalpins-function"></a>EqualPins función)

La función EqualPins comprueba si dos patillas están en el mismo objeto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin1* 
</dt> <dd>

Puntero a un PIN.

</dd> <dt>

*pPin2* 
</dt> <dd>

Puntero al otro PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si ambos PIN están en el mismo objeto o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




