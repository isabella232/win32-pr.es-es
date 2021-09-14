---
description: Puntero al bloque de memoria que contiene los búferes.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: CMemAllocator::m_pBuffer miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362490"
---
# <a name="cmemallocatorm_pbuffer-member"></a>Miembro CMemAllocator::m \_ pBuffer

Puntero al bloque de memoria que contiene los búferes.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a>Observaciones

Los búferes de ejemplo se calculan como desplazamientos desde este puntero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




