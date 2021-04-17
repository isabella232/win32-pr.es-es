---
description: La función GetTrueColorType recupera el nombre legible de un subtipo de vídeo.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Función GetTrueColorType (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653636"
---
# <a name="gettruecolortype-function"></a>GetTrueColorType función)

La función **GetTrueColorType** recupera el nombre legible de un subtipo de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define el mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




