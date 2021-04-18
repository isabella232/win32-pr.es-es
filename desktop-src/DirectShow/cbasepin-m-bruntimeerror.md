---
description: Marca que indica si se ha producido un error en tiempo de ejecución.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Miembro CBasePin:: m_bRunTimeError (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661253"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Miembro bRunTimeError CBasePin:: m \_

Marca que indica si se ha producido un error en tiempo de ejecución.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Observaciones

El valor predeterminado de esta marca **es false**. Establezca la marca en **true** si se produce un error de tiempo de ejecución durante el streaming. El método [**CBasePin:: Inactive**](cbasepin-inactive.md) restablece la marca en **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




