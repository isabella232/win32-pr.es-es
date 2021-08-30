---
description: La función EqualPins comprueba si hay dos pines en el mismo objeto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Función EqualPins (Wxutil.h)
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
ms.openlocfilehash: e304c8d9ed7ef94ee23280d1466450c73e0627d35183c7edfafc4ef13eeba636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079065"
---
# <a name="equalpins-function"></a>Función EqualPins

La función EqualPins comprueba si hay dos pines en el mismo objeto.

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

Puntero a un pin.

</dd> <dt>

*pPin2* 
</dt> <dd>

Puntero al otro pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si ambos pines están en el mismo objeto o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




