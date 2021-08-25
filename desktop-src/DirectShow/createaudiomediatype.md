---
description: La función CreateAudioMediaType inicializa un tipo de medio a partir de una estructura DESATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Función CreateAudioMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908825"
---
# <a name="createaudiomediatype-function"></a>Función CreateAudioMediaType

La **función CreateAudioMediaType** inicializa un tipo de medio a partir de una [**estructura DESATEX.**](/previous-versions/dd757713(v=vs.85))

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwfx* 
</dt> <dd>

Puntero a la estructura [**DESATEX proporcionada.**](/previous-versions/dd757713(v=vs.85))

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a la [**estructura AM MEDIA TYPE \_ \_ que**](/windows/win32/api/strmif/ns-strmif-am_media_type) se inicializará.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Marca que indica si se va a inicializar el bloque de formato. Especifique **TRUE para** inicializar o **FALSE** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ OUTOFMEMORY si no se pudo asignar memoria para los datos de formato; En caso \_ contrario, es correcto.

## <a name="remarks"></a>Comentarios

Si el *parámetro bSetFormat* es **TRUE,** el método asigna la memoria para el bloque de formato. Si el *parámetro pmt* ya contiene un bloque de formato asignado, se producirá una pérdida de memoria. Para evitar una pérdida de memoria, llame [**a FreeMediaType antes**](freemediatype.md) de llamar a esta función. Después de que el método vuelva a llamar **a FreeMediaType** para liberar el bloque de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de tipo multimedia**](media-type-functions.md)
</dt> </dl>

 

