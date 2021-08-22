---
description: La función GetSubtypeName recupera el nombre legible de un subtipo de vídeo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Función GetSubtypeName (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c676f3e08f55bd010e761853b777e0eb4b28933536ab7af09bd94e457032b583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564855"
---
# <a name="getsubtypename-function"></a>Función GetSubtypeName

La `GetSubtypeName` función recupera el nombre legible de un subtipo de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
TCHAR* GetSubtypeName(
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

Devuelve una cadena que contiene el nombre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




