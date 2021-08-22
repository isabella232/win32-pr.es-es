---
description: El método GetAllocatorRequirements recupera las propiedades del asignador solicitadas por el pin de entrada.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Método CBaseInputPin.GetAllocatorRequirements (Amfilter.h)
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
ms.openlocfilehash: 57b085cd82c45fd78ddaa4794084cba775e1c80cd8b9e3b8df4c9680379ba462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586375"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>Método CBaseInputPin.GetAllocatorRequirements

El `GetAllocatorRequirements` método recupera las propiedades del asignador solicitadas por el pin de entrada.

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

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que se rellena con los requisitos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Comentarios

Cuando un pin de salida inicializa un asignador de memoria, puede llamar a este método para determinar si el pin de entrada tiene algún requisito de búfer. Para obtener más información, [**vea CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

La implementación de este método es opcional. Si el filtro tiene requisitos específicos de alineación o prefijo, invalide este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




