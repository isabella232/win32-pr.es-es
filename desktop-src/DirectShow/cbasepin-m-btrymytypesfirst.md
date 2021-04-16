---
description: Marca que indica si el PIN intenta sus propios tipos de medios preferidos antes de los del PIN receptor.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Miembro CBasePin:: m_bTryMyTypesFirst (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671446"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Miembro bTryMyTypesFirst CBasePin:: m \_

Marca que indica si el PIN intenta sus propios tipos de medios preferidos antes de los del PIN receptor.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Observaciones

El valor predeterminado de esta marca **es false**. Si la marca es **true**, el método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) invierte el orden en el que prueba los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




