---
description: La función CreateMediaType asigna una nueva estructura \_ AM MEDIA \_ TYPE, incluido el bloque de formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Función CreateMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0384b0a72e10b84cd94581816c0441de6a19fa5148a97fa9e55d72bdd63d678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871415"
---
# <a name="createmediatype-function"></a>Función CreateMediaType

La **función CreateMediaType** asigna una nueva estructura [**AM MEDIA \_ \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) incluido el bloque de formato.

## <a name="syntax"></a>Sintaxis


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) El método copia esta estructura en la nueva estructura .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una nueva [**estructura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) o **NULL** si se produce un error.

## <a name="remarks"></a>Comentarios

Para liberar la memoria asignada por esta función, llame a [**DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

 




