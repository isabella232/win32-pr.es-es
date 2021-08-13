---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método usa el parámetro "pguid".
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Constructor FOURCCMap::FOURCCMap (Fourcc.h): parámetro pguid'
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
ms.openlocfilehash: 2c674791418a7668d7c7597e951e9a89613b9c8150865ff123263e9d0ef9ded2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330445"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Constructor FOURCCMap::FOURCCMap (Fourcc.h): parámetro pguid

Método constructor. El constuctor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y **los subtipos GUID.**

## <a name="syntax"></a>Sintaxis


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguid* 
</dt> <dd>

Puntero al identificador único global **(GUID).**

</dd> </dl>

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

 

 




