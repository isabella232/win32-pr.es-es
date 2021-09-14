---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método no usa parámetros.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Constructor FOURCCMap::FOURCCMap (Fourcc.h): sin parámetros'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063268"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Constructor FOURCCMap::FOURCCMap (Fourcc.h): sin parámetros

Método constructor. El constuctor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y **los subtipos GUID.**

## <a name="syntax"></a>Sintaxis


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parámetros

Este constructor no tiene parámetros.

## <a name="remarks"></a>Observaciones

Si este objeto se construye con el código **FOURCC,** se crea un **GUID** para que coincida con él. Si este objeto se crea con un **GUID existente,** el **valor FOURCC** del objeto se establece en cero. A partir de entonces, **el valor FOURCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC,**](fourccmap-getfourcc.md) respectivamente.

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|-|-|
| Encabezado  | Fourcc.h (incluir Secuencias.h) |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FOURCCMap (clase)**](fourccmap.md)
</dt> </dl>

 

 




