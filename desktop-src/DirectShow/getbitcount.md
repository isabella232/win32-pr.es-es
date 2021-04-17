---
description: La función GetBitCount devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado. Esta función solo es válida para los subtipos RGB no comprimidos.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Función GetBitCount (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680218"
---
# <a name="getbitcount-function"></a>GetBitCount función)

La `GetBitCount` función devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado. Esta función solo es válida para los subtipos RGB no comprimidos.

## <a name="syntax"></a>Sintaxis


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubtype* 
</dt> <dd>

Puntero a un **GUID** de subtipo de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bits por píxel para este subtipo, o el valor **USHRT \_ Max** si no se reconoce el subtipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




