---
description: Recupera el valor de FOURCC&\# 160; DWORD del objeto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'FOURCCMap:: GetFOURCC (método) (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653443"
---
# <a name="fourccmapgetfourcc-method"></a>FOURCCMap:: GetFOURCC (método)

Recupera el **valor DWORD** de **FourCC** del objeto [**FOURCCMap**](fourccmap.md) .

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **DWORD** de **FourCC** . Tenga en cuenta que si crea un **GUID** que no se derivó originalmente de un **FourCC**, el valor devuelto será esencialmente aleatorio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>FourCC. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




