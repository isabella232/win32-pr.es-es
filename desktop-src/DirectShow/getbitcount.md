---
description: La función GetBitCount devuelve el número de bits por píxel usados por un subtipo de vídeo especificado. Esta función solo es válida para subtipos RGB sin comprimir.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Función GetBitCount (Wxutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063254"
---
# <a name="getbitcount-function"></a>Función GetBitCount

La `GetBitCount` función devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado. Esta función solo es válida para subtipos RGB sin comprimir.

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

Puntero a un GUID de subtipo **de vídeo.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bits por píxel de este subtipo o el valor **USHRT \_ MAX** si no se reconoce el subtipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




