---
description: La función FreeMediaType elimina el bloque de formato en una \_ estructura de tipo de medio am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Función FreeMediaType (mtype. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680873"
---
# <a name="freemediatype-function"></a>FreeMediaType función)

La función **FreeMediaType** elimina el bloque de formato en una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

## <a name="syntax"></a>Sintaxis


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MT* \[ CLI\]
</dt> <dd>

Referencia a una estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El bloque de formato se asigna en el montón. El miembro **pbFormat** del [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) apunta al bloque de formato. Use esta función para liberar solo el bloque de formato. Para eliminar una estructura **de \_ \_ tipo de medio am** asignada, llame a [**DeleteMediaType**](deletemediatype.md).

Esta función se define en la biblioteca de [clases base de DirectShow](directshow-base-classes.md) . Si prefiere no vincular a la biblioteca de clases base, puede usar el código siguiente:


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
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

 




