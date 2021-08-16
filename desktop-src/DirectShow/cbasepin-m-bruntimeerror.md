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
ms.openlocfilehash: ffc07a15f7c34744be52c5e2c7b5233e1885b58c5b9b7d078871277f8fc0efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823337"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Miembro CBasePin::m \_ bRunTimeError

Marca que indica si se ha producido un error en tiempo de ejecución.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Comentarios

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

 

 




