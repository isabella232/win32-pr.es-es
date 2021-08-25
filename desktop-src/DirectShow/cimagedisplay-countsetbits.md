---
description: El método CountSetBits devuelve el número de bits establecido en 1 en un campo de bits especificado.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Método CImageDisplay.CountSetBits (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d334111c18c2c94c79a8b49ed7c0601efabb2bd13922a68c292970d4d2c379bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824075"
---
# <a name="cimagedisplaycountsetbits-method"></a>Método CImageDisplay.CountSetBits

El `CountSetBits` método devuelve el número de bits establecido en 1 en un campo de bits especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Campo* 
</dt> <dd>

Especifica un campo de bits como un **valor DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bits que se establecen en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




