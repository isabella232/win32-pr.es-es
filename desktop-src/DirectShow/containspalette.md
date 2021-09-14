---
description: La función ContainsPalette determina si una estructura VIDEOINFOHEADER especificada contiene una paleta.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Función ContainsPalette (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161578"
---
# <a name="containspalette-function"></a>Función ContainsPalette

La **función ContainsPalette** determina si una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contiene una paleta.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntero a una [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si bitdepth es 8 o menos (**bmiHeader.biBitCount**), o si el número de índices de color es mayor que cero (**bmiHeader.biClrUsed**). Devuelve **FALSE en caso** contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




