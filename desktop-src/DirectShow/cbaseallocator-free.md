---
description: El método Free libera toda la memoria del búfer. Se llama a este método cuando el filtro propietario desasigna el asignador, después de que se libera el último ejemplo multimedia.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Método CBaseAllocator.Free (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361426"
---
# <a name="cbaseallocatorfree-method"></a>CBaseAllocator.Free (método)

El `Free` método libera toda la memoria del búfer. Se llama a este método cuando el filtro propietario desasigna el asignador, después de que se libera el último ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Después de [**llamar al método Decommit,**](cbaseallocator-decommit.md) el asignador llama a este método cuando libera el último ejemplo multimedia. La clase derivada debe implementar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




