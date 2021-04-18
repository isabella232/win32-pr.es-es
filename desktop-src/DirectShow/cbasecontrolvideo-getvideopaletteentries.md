---
description: El método GetVideoPaletteEntries recupera un intervalo de entradas de la paleta para el vídeo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Método CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690844"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>CBaseControlVideo. GetVideoPaletteEntries, método

El `GetVideoPaletteEntries` método recupera un intervalo de entradas de la paleta para el vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Super* 
</dt> <dd>

Entrada de la paleta de inicio de base cero.

</dd> <dt>

*Entradas* 
</dt> <dd>

Número de entradas necesarias.

</dd> <dt>

*pRetrieved* 
</dt> <dd>

Puntero al número de colores obtenidos.

</dd> <dt>

*pPalette* 
</dt> <dd>

Puntero en el búfer de salida para los colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NoError si se realiza correctamente, VFW \_ e \_ no hay ninguna \_ paleta \_ disponible si los ejemplos de vídeo no tienen paleta de colores, e \_ OUTOFMEMORY si no hay suficiente memoria disponible, e \_ INVALIDARG si *StartIndex* no es válido o S \_ false si no hay colores en la paleta.

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve la paleta actual del vídeo como una matriz asignada por el usuario. Para mantener la coherencia, use los miembros de la estructura de Win32 **PALETTEENTRY** para devolver los colores, en lugar de los miembros de la estructura **RGBQUAD** (aunque el parámetro es un **valor Long**). El autor de la llamada asigna la memoria, por lo que basta con copiar cada uno de ellos a su vez. Determine que el número de entradas solicitadas y el desplazamiento de la posición de inicio son válidos. Si el número de entradas se evalúa como cero, se devuelve un \_ código S false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




