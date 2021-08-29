---
description: El método GetProperties recupera el número de búferes que creará el asignador y las propiedades del búfer. Este método implementa el método IMemAllocator::GetProperties.
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Método CBaseAllocator.GetProperties (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 469eb062113ab2ee87e6462b0e0227eaba11673a239794c844125823c4b8a05f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832755"
---
# <a name="cbaseallocatorgetproperties-method"></a>Método CBaseAllocator.GetProperties

El método recupera el número de búferes que creará el `GetProperties` asignador y las propiedades del búfer. Este método implementa el [**método IMemAllocator::GetProperties.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProps* 
</dt> <dd>

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que recibe las propiedades del asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




