---
description: El método DecideAllocator negocia un asignador con el PIN de salida.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Método CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680836"
---
# <a name="cpullpindecideallocator-method"></a>CPullPin. DecideAllocator, método

El `DecideAllocator` método negocia un asignador con el PIN de salida.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador preferido del PIN de entrada o **null**.

</dd> <dt>

*pProps* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) opcional que contiene los requisitos de búfer del PIN de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Este método llama al método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) para negociar un asignador. Pasa el parámetro *pAlloc* directamente al método **RequestAllocator** . Pasa el parámetro *pProps* a **RequestAllocator** si *pProps* no es **null**; de lo contrario, crea una estructura de **\_ propiedades de asignador** con una solicitud predeterminada de tres búferes de 64 k.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> <dt>

[**CPullPin:: Connect**](cpullpin-connect.md)
</dt> </dl>

 

 




