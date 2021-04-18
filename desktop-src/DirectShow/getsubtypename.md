---
description: La función GetSubtypeName recupera el nombre legible de un subtipo de vídeo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Función GetSubtypeName (Wxutil. h)
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
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653836"
---
# <a name="getsubtypename-function"></a>GetSubtypeName función)

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

Puntero a un **GUID** de subtipo de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena que contiene el nombre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




