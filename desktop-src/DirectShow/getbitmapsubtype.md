---
description: La función GetBitmapSubtype devuelve el GUID del subtipo multimedia para el mapa de bits especificado.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Función GetBitmapSubtype (Wxutil.h)
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
ms.openlocfilehash: 8903e4a404367327b677a239b8ab28e3cb47e5679203857154f453a5cc01e25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536685"
---
# <a name="getbitmapsubtype-function"></a>Función GetBitmapSubtype

La `GetBitmapSubtype` función devuelve el GUID del subtipo de **medio** para el mapa de bits especificado.

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

Puntero a una [**estructura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el GUID del subtipo **de medio**.

## <a name="remarks"></a>Comentarios

Para los tipos RGB sin comprimir, esta función asigna **el campo biBitCount** al subtipo. Para los tipos de vídeo comprimidos, esta función usa la [**clase FOURCCMap**](fourccmap.md) para asignar el **campo biCompression** al subtipo.

Si la función no puede hacer coincidir el formato con un subtipo, el valor devuelto es GUID \_ NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




