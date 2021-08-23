---
description: El método IncrementTypeVersion incrementa el número de versión en el conjunto de tipos de medios preferidos.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Método CBasePin.IncrementTypeVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a8c2536b91d5630141e5a62fa1aa895555537b61f89a574f4cdc1ec208810c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526865"
---
# <a name="cbasepinincrementtypeversion-method"></a>Método CBasePin.IncrementTypeVersion

El `IncrementTypeVersion` método incrementa el número de versión en el conjunto de tipos de medios preferidos.

## <a name="syntax"></a>Sintaxis


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método incrementa la variable [**miembro CBasePin::m \_ TypeVersion.**](cbasepin-m-typeversion.md) Si el pin cambia dinámicamente la lista de tipos de medios preferidos, llame a este método cada vez que cambie la lista. Para obtener más información, [**vea CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




