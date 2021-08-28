---
description: El método CheckPaletteHeader valida las entradas de la paleta en una estructura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Método CImageDisplay.CheckPaletteHeader (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6378a93ffced86546b8e95071e7f9bdc1398cdd1831aa18d41d62c6ea97caff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087295"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Método CImageDisplay.CheckPaletteHeader

El `CheckPaletteHeader` método valida las entradas de la paleta en una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInput* 
</dt> <dd>

Puntero a una **estructura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** las entradas de la paleta son válidas o FALSE **en** caso contrario.

## <a name="remarks"></a>Comentarios

Si el formato de imagen no está desanclado, el método comprueba que **biClrUsed** es igual a cero. De lo contrario, el método comprueba que la **marca biCompression** es BI \_ RGB; **biClrImportant** no es mayor que **biClrUsed**; y el número de entradas de paleta no supera el máximo, dada la profundidad de color.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




