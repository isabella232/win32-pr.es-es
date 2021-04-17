---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método usa el parámetro ' FourCC '.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Constructor FOURCCMap:: FOURCCMap (FourCC. h): parámetro FourCC'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105653292"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>Constructor FOURCCMap:: FOURCCMap (FourCC. h): parámetro FourCC

Método de constructor. Constructor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y los subtipos de **GUID** .

## <a name="syntax"></a>Sintaxis


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FourCC* 
</dt> <dd>

**DWORD** que especifica el FourCC.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si este objeto se construye con el código **FourCC** , se crea un **GUID** para que coincida. Si este objeto se crea con un **GUID** existente, el valor de **FourCC** del objeto se establece en cero. Después, el valor de **FourCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado  | FourCC. h (incluir streams. h) |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




