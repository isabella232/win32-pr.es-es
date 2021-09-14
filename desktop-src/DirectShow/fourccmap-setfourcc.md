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
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063260"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FOURCCMap (clase)**](fourccmap.md)
</dt> </dl>

 

 




