---
description: Establece la parte FOURCC del objeto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: Método FOURCCMap::SetFOURCC (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ac14c7174fde7184bfdbfbb5d82d3fc1288d46ff37158bbbab146c34db5ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536835"
---
# <a name="fourccmapsetfourcc-method"></a>Método FOURCCMap::SetFOURCC

Establece la **parte FOURCC** del [**objeto FOURCCMap.**](fourccmap.md)

## <a name="syntax"></a>Sintaxis


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguid* 
</dt> <dd>

Puntero a la parte del identificador único global **(GUID)** devuelto del **objeto FOURCCMap.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Fourcc.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FOURCCMap (clase)**](fourccmap.md)
</dt> </dl>

 

 




