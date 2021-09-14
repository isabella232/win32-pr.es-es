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
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062408"
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

## <a name="remarks"></a>Observaciones

Si el *parámetro bSetFormat* es **TRUE,** el método asigna la memoria para el bloque de formato. Si el *parámetro pmt* ya contiene un bloque de formato asignado, se producirá una pérdida de memoria. Para evitar una pérdida de memoria, llame [**a FreeMediaType antes**](freemediatype.md) de llamar a esta función. Después de que el método vuelva a llamar **a FreeMediaType** para liberar el bloque de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones de tipo multimedia**](media-type-functions.md)
</dt> </dl>

 

