---
description: La función CopyMediaType copia una estructura \_ AM MEDIA TYPE en otra \_ estructura, incluido el bloque de formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Función CopyMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b193f64edb55a342546f26db1975080490f0e69b2caa91695b3bc63240750983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634384"
---
# <a name="copymediatype-function"></a>Función CopyMediaType

La **función CopyMediaType** copia una estructura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) en otra estructura, incluido el bloque de formato

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmtTarget* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) El método copia el tipo de medio en esta estructura.

</dd> <dt>

*pmtSource* 
</dt> <dd>

Puntero a una estructura [**AM \_ MEDIA TYPE \_ de**](/windows/win32/api/strmif/ns-strmif-am_media_type) origen que se copiará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función asigna la memoria para el bloque de formato. Si el *parámetro pmtTarget* ya contiene un bloque de formato asignado, se producirá una pérdida de memoria. Para evitar una pérdida de memoria, llame [**a FreeMediaType antes**](freemediatype.md) de llamar a esta función.

Una vez que el método vuelva, llame [**a FreeMediaType**](freemediatype.md) en *pmtTarget* para liberar el bloque de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

 




