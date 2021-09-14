---
description: La función FreeMediaType elimina el bloque de formato en una estructura \_ AM MEDIA \_ TYPE.
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Función FreeMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061169"
---
# <a name="freemediatype-function"></a>Función FreeMediaType

La **función FreeMediaType** elimina el bloque de formato en una [**estructura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

## <a name="syntax"></a>Sintaxis


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mt* \[ Ref\]
</dt> <dd>

Referencia a una estructura [**\_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El bloque de formato se asigna en el montón. El **miembro pbFormat** de [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) apunta al bloque de formato. Use esta función para liberar solo el bloque de formato. Para eliminar una estructura **AM \_ MEDIA TYPE \_ asignada,** llame a [**DeleteMediaType**](deletemediatype.md).

Esta función se define en la biblioteca [DirectShow clases base.](directshow-base-classes.md) Si prefiere no vincular a la biblioteca de clases base, puede usar el código siguiente:


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

 




