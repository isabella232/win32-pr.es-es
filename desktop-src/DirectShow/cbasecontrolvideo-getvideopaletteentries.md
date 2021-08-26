---
description: El método GetVideoPaletteEntries recupera un intervalo de entradas de paleta para el vídeo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Método CBaseControlVideo.GetVideoPaletteEntries (Ctlutil.h)
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
ms.openlocfilehash: 5eb1c017353ed3e5095f5ee5d24870773c11211c14eaa44a673b4f12913c56c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057045"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>Método CBaseControlVideo.GetVideoPaletteEntries

El `GetVideoPaletteEntries` método recupera un intervalo de entradas de paleta para el vídeo.

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

*Startindex* 
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

Puntero al búfer de salida para los colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR si se realiza correctamente, VFW E NO PALETTE AVAILABLE si los ejemplos de vídeo no tienen paleta de \_ \_ \_ \_ colores, \_ E OUTOFMEMORY \_  si no hay suficiente memoria disponible, E INVALIDARG si StartIndex no es válido o S \_ FALSE si no hay colores en la paleta.

## <a name="remarks"></a>Comentarios

Esta función miembro devuelve la paleta actual del vídeo como una matriz asignada por el usuario. Para mantener la coherencia, use los miembros de la estructura **PALETTEENTRY** de Win32 para devolver los colores, en lugar de los miembros de la estructura **RGBQUAD** (aunque el parámetro es **LONG**). El autor de la llamada asigna la memoria, por lo que basta con copiar cada una a su vez. Determine que el número de entradas solicitadas y el desplazamiento de la posición inicial son válidos. Si el número de entradas se evalúa como cero, devuelva un código S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




