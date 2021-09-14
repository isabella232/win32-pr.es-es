---
description: La función DeleteMediaType elimina una estructura AM \_ MEDIA \_ TYPE asignada, incluido el bloque de formato.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Función DeleteMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061243"
---
# <a name="deletemediatype-function"></a>Función DeleteMediaType

La **función DeleteMediaType** elimina una estructura [**AM MEDIA TYPE \_ \_ asignada,**](/windows/win32/api/strmif/ns-strmif-am_media_type) incluido el bloque de formato.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a una estructura [**\_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use esta función para liberar cualquier estructura de tipo de medio que se asignó mediante [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) o [**CreateMediaType**](createmediatype.md).

Esta función se define en la biblioteca [DirectShow base.](directshow-base-classes.md) Si prefiere no vincular a la biblioteca de clases base, puede usar el código siguiente:


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


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
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

[**FreeMediaType**](freemediatype.md)
</dt> <dt>

[**Funciones de tipo de medio**](media-type-functions.md)
</dt> </dl>

 

