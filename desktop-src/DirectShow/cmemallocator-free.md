---
description: Se llama al método Free durante una operación de confirmación.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Método CMemAllocator.Free (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255476"
---
# <a name="cmemallocatorfree-method"></a>CMemAllocator.Free (método)

Se `Free` llama al método durante una operación de confirmación. Este método implementa el método [**virtual puro CBaseAllocator::Free,**](cbaseallocator-free.md) pero no hace nada. La memoria del búfer no se libera realmente hasta que se destruye el objeto **CMemAllocator.** El método destructor llama [**a CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) para liberar la memoria.

## <a name="syntax"></a>Sintaxis


```C++
void Free();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




