---
description: El método DecideAllocator negocia un asignador con el pin de salida.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Método CPullPin.DecideAllocator (Pullpin.h)
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
ms.openlocfilehash: e02fe78631c6ddee01b7acc96d761f71b80e8d3e1738d2ed6f6ae40d70b0c5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055065"
---
# <a name="cpullpindecideallocator-method"></a>CPullPin.DecideAllocator (método)

El `DecideAllocator` método negocia un asignador con el pin de salida.

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

Puntero a la [**interfaz IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador preferido del pin de entrada, o **NULL.**

</dd> <dt>

*pProps* 
</dt> <dd>

Puntero a una estructura [**OPCIONAL ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error en caso contrario.

## <a name="remarks"></a>Comentarios

Este método llama al [**método IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) para negociar un asignador. Pasa el parámetro *pAlloc* directamente al **método RequestAllocator.** Pasa el parámetro *pProps* a **RequestAllocator** si *pProps* no es **NULL**; De lo contrario, crea una **estructura ALLOCATOR \_ PROPERTIES** con una solicitud predeterminada de tres búferes de 64 K.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> <dt>

[**CPullPin::Conectar**](cpullpin-connect.md)
</dt> </dl>

 

 




