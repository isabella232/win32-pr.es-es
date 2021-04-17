---
description: Marca que indica si hay una operación de desconfirmación en curso.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Miembro CBaseAllocator:: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670629"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Miembro bDecommitInProgress CBaseAllocator:: m \_

Marca que indica si hay una operación de desconfirmación en curso. El valor es **true** una vez que se llama al método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , pero antes de que se liberen todos los búferes. Si el valor es **true**, se produce un error en el método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) . Además, el asignador no debe eliminarse a sí mismo mientras que el valor es **true**.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




