---
description: Estado de bloqueo.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Miembro CDynamicOutputPin:: m_BlockState (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661321"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a>Miembro BlockState CDynamicOutputPin:: m \_

Estado de bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a>Observaciones

Se definen los siguientes Estados:

-   NO \_ bloqueado
-   PENDING
-   BLOQUEO

Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




