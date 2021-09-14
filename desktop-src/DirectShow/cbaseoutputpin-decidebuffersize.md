---
description: 'Método CBaseOutputPin.DecideBufferSize: el método DecideBufferSize establece los requisitos del búfer.'
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Método CBaseOutputPin.DecideBufferSize (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160204"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>CBaseOutputPin.DecideBufferSize (método)

El `DecideBufferSize` método establece los requisitos del búfer.

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

Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada. Si el pin de entrada no tiene ningún requisito, el autor de la llamada debe cero los miembros de esta estructura antes de llamar al método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Invalide este método en la clase derivada. Llame al [**método IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) para especificar los requisitos del búfer. Normalmente, la clase derivada respetará los requisitos de búfer del pin de entrada, pero no es necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




