---
description: El método GetFreeCount recupera el número de muestras de medios que no están en uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Método CBaseAllocator.GetFreeCount (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070169"
---
# <a name="cbaseallocatorgetfreecount-method"></a>Método CBaseAllocator.GetFreeCount

El `GetFreeCount` método recupera el número de muestras de medios que no están en uso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plBuffersFree* 
</dt> <dd>

Dirección de una variable que recibe el número de muestras que no están en uso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método implementa el [**método IMemAllocatorCallbackTemp::GetFreeCount.**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) El asignador no expone la interfaz IMemAllocatorCallbackTemp a menos que la marca *fEnableReleaseCallback* esté establecida en **TRUE** en el constructor CBaseAllocator.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




