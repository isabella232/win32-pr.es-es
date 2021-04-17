---
description: El método CountSetBits devuelve el número de bits establecido en 1 en un campo de bits especificado.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Método CImageDisplay. CountSetBits (Winutil. h)
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
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681134"
---
# <a name="cimagedisplaycountsetbits-method"></a>CImageDisplay. CountSetBits, método

El `CountSetBits` método devuelve el número de bits establecidos en 1 en un campo de bits especificado.

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

Especifica un campo de bits como un valor **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bits que se establecen en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




