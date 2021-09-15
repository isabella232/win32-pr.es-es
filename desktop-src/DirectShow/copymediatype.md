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
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473999"
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

## <a name="remarks"></a>Observaciones

Esta función asigna la memoria para el bloque de formato. Si el *parámetro pmtTarget* ya contiene un bloque de formato asignado, se producirá una pérdida de memoria. Para evitar una pérdida de memoria, llame [**a FreeMediaType antes**](freemediatype.md) de llamar a esta función.

Una vez que el método vuelva, llame [**a FreeMediaType**](freemediatype.md) en *pmtTarget* para liberar el bloque de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

 




