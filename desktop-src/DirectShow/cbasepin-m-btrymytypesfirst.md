---
description: Marca que indica si el pin intenta sus propios tipos de medios preferidos antes que los del pin receptor.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: CBasePin::m_bTryMyTypesFirst miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df94a95783d15c09fd53bd8659db71f2ce0b1aefe5d855fef5f5a03e71445493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158376"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Miembro CBasePin::m \_ bTryMyTypesFirst

Marca que indica si el pin intenta sus propios tipos de medios preferidos antes que los del pin receptor.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Comentarios

El valor predeterminado de esta **marca es FALSE.** Si la marca es **TRUE**, el método [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) invierte el orden en el que intenta los tipos multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




