---
description: La función GetBitmapSubtype devuelve el GUID del subtipo de medios para el mapa de bits especificado.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Función GetBitmapSubtype (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680213"
---
# <a name="getbitmapsubtype-function"></a>GetBitmapSubtype función)

La `GetBitmapSubtype` función devuelve el **GUID** del subtipo de medios para el mapa de bits especificado.

## <a name="syntax"></a>Sintaxis


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **GUID** del subtipo de medio.

## <a name="remarks"></a>Observaciones

En el caso de los tipos RGB sin comprimir, esta función asigna el campo **biBitCount** al subtipo. En el caso de los tipos de vídeo comprimidos, esta función usa la clase [**FOURCCMap**](fourccmap.md) para asignar el campo de **bicompresión** al subtipo.

Si la función no puede coincidir con el formato de un subtipo, el valor devuelto es GUID \_ null.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




