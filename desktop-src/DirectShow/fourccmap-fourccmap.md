---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método no usa ningún parámetro.
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
ms.openlocfilehash: d856589146103e599a1cf67d2090dd64af7107d1c221c46b9c93852f989ade9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015733"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Constructor FOURCCMap::FOURCCMap (Fourcc.h): sin parámetros

Método constructor. El constuctor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y **los subtipos GUID.**

## <a name="syntax"></a>Sintaxis


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parámetros

Este constructor no tiene parámetros.

## <a name="remarks"></a>Comentarios

Si este objeto se construye con el código **FOURCC,** se crea un **GUID** para que coincida con él. Si este objeto se crea con un **GUID existente,** el **valor FOURCC** del objeto se establece en cero. A partir de entonces, el **valor FOURCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC,**](fourccmap-getfourcc.md) respectivamente.

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|-|-|
| Encabezado  | Fourcc.h (incluir Secuencias.h) |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FOURCCMap (clase)**](fourccmap.md)
</dt> </dl>

 

 




