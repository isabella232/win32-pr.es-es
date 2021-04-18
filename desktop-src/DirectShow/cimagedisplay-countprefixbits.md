---
description: El método CountPrefixBits calcula el número de bits cero al principio de un campo de bits especificado.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Método CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660935"
---
# <a name="cimagedisplaycountprefixbits-method"></a>CImageDisplay. CountPrefixBits, método

El `CountPrefixBits` método calcula el número de bits cero al principio de un campo de bits especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD CountPrefixBits(
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

Devuelve el número de bits cero que se producen antes del primer bit 1 o 0x80000000 si todos los bits son cero.

## <a name="remarks"></a>Observaciones

Este método es útil para trabajar con máscaras de colores en estructuras de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




