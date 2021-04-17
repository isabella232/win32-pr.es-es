---
description: El método GetAllocatorRequirements recupera las propiedades de asignador solicitadas por el PIN de entrada.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Método CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660343"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>CBaseInputPin. GetAllocatorRequirements, método

El `GetAllocatorRequirements` método recupera las propiedades de asignador solicitadas por el PIN de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProps* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que se rellena con los requisitos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Observaciones

Cuando un terminal de salida Inicializa un asignador de memoria, puede llamar a este método para determinar si el PIN de entrada tiene algún requisito de búfer. Para obtener más información, vea [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

La implementación de este método es opcional. Si el filtro tiene requisitos de alineación o prefijo específicos, Invalide este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




