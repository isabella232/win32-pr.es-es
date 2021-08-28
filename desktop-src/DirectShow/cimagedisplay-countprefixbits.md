---
description: El método CountPrefixBits calcula el número de cero bits al principio de un campo de bits especificado.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Método CImageDisplay.CountPrefixBits (Winutil.h)
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
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108485"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Método CImageDisplay.CountPrefixBits

El `CountPrefixBits` método calcula el número de cero bits al principio de un campo de bits especificado.

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

Especifica un campo de bits como un **valor DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bits cero que se producen antes del primer bit o 0x80000000 si todos los bits son cero.

## <a name="remarks"></a>Comentarios

Este método es útil para trabajar con máscaras de color en [**estructuras VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




