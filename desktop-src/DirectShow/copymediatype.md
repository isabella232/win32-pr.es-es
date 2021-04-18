---
description: La función CopyMediaType copia una \_ estructura de tipo de medio am \_ en otra estructura, incluido el bloque de formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Función CopyMediaType (mtype. h)
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
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680586"
---
# <a name="copymediatype-function"></a>CopyMediaType función)

La función **CopyMediaType** copia una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) en otra estructura, incluido el bloque de formato

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

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . El método copia el tipo de archivo multimedia en esta estructura.

</dd> <dt>

*pmtSource* 
</dt> <dd>

Puntero a la estructura [**de \_ \_ tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type) de origen AM que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función asigna la memoria para el bloque de formato. Si el parámetro *pmtTarget* ya contiene un bloque de formato asignado, se producirá una fuga de memoria. Para evitar una pérdida de memoria, llame a [**FreeMediaType**](freemediatype.md) antes de llamar a esta función.

Después de que el método vuelva, llame a [**FreeMediaType**](freemediatype.md) en *pmtTarget* para liberar el bloque de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

 




