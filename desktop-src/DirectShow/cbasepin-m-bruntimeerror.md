---
description: Marca que indica si se ha producido un error en tiempo de ejecución.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: CBasePin::m_bRunTimeError miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973978"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Miembro CBasePin::m \_ bRunTimeError

Marca que indica si se ha producido un error en tiempo de ejecución.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Observaciones

El valor predeterminado de esta **marca es FALSE.** Establezca la marca en **TRUE si** se produce un error en tiempo de ejecución durante el streaming. El [**método CBasePin::Inactive**](cbasepin-inactive.md) restablece la marca a **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




