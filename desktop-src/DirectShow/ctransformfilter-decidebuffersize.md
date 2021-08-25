---
description: 'Método CTransformFilter.DecideBufferSize: el método DecideBufferSize establece los requisitos de búfer del pin de salida.'
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Método CTransformFilter.DecideBufferSize (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1aba3ec43318079a73f0c94c8446b637ece29a5b61752462eeb8fc5898f5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907705"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>Método CTransformFilter.DecideBufferSize

El `DecideBufferSize` método establece los requisitos de búfer del pin de salida.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntero a la [**interfaz IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) en el asignador de la patilla de salida.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada de bajada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

El método [**CTransformOutputPin::D ecideBufferSize**](ctransformoutputpin-decidebuffersize.md) del pin de salida llama a este método. La clase derivada debe implementar este método. Para obtener más información, [**vea CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




