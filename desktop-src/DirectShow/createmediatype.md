---
description: La función CreateMediaType asigna una nueva estructura AM \_ MEDIA \_ TYPE, incluido el bloque de formato.
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
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246734"
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

Puntero a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) El método copia esta estructura en la nueva estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una nueva [**estructura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) o **NULL** si se produce un error.

## <a name="remarks"></a>Observaciones

Para liberar la memoria asignada por esta función, llame a [**DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de tipo multimedia**](media-type-functions.md)
</dt> </dl>

 

 




