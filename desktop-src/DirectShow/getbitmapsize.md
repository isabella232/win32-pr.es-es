---
description: La función GetBitmapSize calcula el número de bytes requeridos por un mapa de bits independiente del dispositivo (DIB). Esta función simplemente llama a la macro DIBSIZE.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Función GetBitmapSize (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061156"
---
# <a name="getbitmapsize-function"></a>Función GetBitmapSize

La `GetBitmapSize` función calcula el número de bytes requeridos por un mapa de bits independiente del dispositivo (DIB). Esta función simplemente llama a la macro [**DIBSIZE.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetBitmapSize(
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

Devuelve el tamaño en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




