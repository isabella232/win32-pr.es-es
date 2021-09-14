---
description: Recupera la propiedad FOURCC&\# 160;DWORD del objeto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: Método FOURCCMap::GetFOURCC (Fourcc.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061670"
---
# <a name="fourccmapgetfourcc-method"></a>FourccMap::GetFOURCC (método)

Recupera **FOURCC** **DWORD del** objeto [**FOURCCMap.**](fourccmap.md)

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor FOURCC** **DWORD.** Tenga en cuenta que si construye un **GUID** que no se deriva originalmente de **fourcc,** el valor devuelto será esencialmente aleatorio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Fourcc.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FOURCCMap (clase)**](fourccmap.md)
</dt> </dl>

 

 




