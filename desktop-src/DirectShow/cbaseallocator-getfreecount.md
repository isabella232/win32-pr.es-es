---
description: El método GetFreeCount recupera el número de muestras multimedia que no están en uso.
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
ms.openlocfilehash: c4552829482a604b368a6710c62d0fc0b26a94aa3bb33b67ef386f2785d6c90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057515"
---
# <a name="cbaseallocatorgetfreecount-method"></a>CBaseAllocator.GetFreeCount (método)

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

## <a name="remarks"></a>Comentarios

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

 

 




