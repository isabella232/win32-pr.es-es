---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método usa el parámetro "Fourcc".
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Constructor FOURCCMap::FOURCCMap (Fourcc.h): parámetro Fourcc'
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
ms.openlocfilehash: 9cfd9cbb93a4d517391be0afe591d3378d9ecef32a0013ab452d31b9eecb6d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043215"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>Constructor FOURCCMap::FOURCCMap (Fourcc.h): parámetro Fourcc

Método constructor. El constuctor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y **los subtipos GUID.**

## <a name="syntax"></a>Sintaxis


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Fourcc* 
</dt> <dd>

**DWORD** que especifica fourcc.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si este objeto se construye con el código **FOURCC,** se crea un **GUID** para que coincida con él. Si este objeto se crea con un **GUID** existente, el **valor FOURCC** del objeto se establece en cero. A partir de entonces, **el valor FOURCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC,**](fourccmap-getfourcc.md) respectivamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado  | Fourcc.h (incluir Secuencias.h) |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**FOURCCMap (clase)**](fourccmap.md)
</dt> </dl>

 

 




