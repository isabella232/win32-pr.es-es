---
description: Marca que indica si el pin intenta sus propios tipos de medios preferidos antes que los del pin receptor.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: Miembro CBasePin::m_bTryMyTypesFirst (Amfilter.h)
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
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973969"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Miembro CBasePin::m \_ bTryMyTypesFirst

Marca que indica si el pin intenta sus propios tipos de medios preferidos antes que los del pin receptor.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Observaciones

El valor predeterminado de esta **marca es FALSE.** Si la marca es **TRUE,** el método [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) invierte el orden en el que intenta los tipos multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




