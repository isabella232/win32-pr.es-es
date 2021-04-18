---
description: La función CreateAudioMediaType Inicializa un tipo de archivo multimedia a partir de una estructura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Función CreateAudioMediaType (mtype. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680862"
---
# <a name="createaudiomediatype-function"></a>CreateAudioMediaType función)

La función **CreateAudioMediaType** Inicializa un tipo de archivo multimedia a partir de una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

Puntero a la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) proporcionada.

</dd> <dt>

*p.p.* 
</dt> <dd>

Puntero a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se va a inicializar.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Marca que indica si se debe inicializar el bloque de formato. Especifique **true** para inicializarlo o **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ OUTOFMEMORY si no se pudo asignar memoria para los datos de formato; \_En caso contrario, es correcto.

## <a name="remarks"></a>Observaciones

Si el parámetro *bSetFormat* es **true**, el método asigna la memoria para el bloque de formato. Si el parámetro *PMT* ya contiene un bloque de formato asignado, se producirá una fuga de memoria. Para evitar una pérdida de memoria, llame a [**FreeMediaType**](freemediatype.md) antes de llamar a esta función. Cuando el método vuelva, llame de nuevo a **FreeMediaType** para liberar el bloque de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

