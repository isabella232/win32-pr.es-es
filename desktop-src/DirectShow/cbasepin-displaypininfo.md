---
description: El método DisplayPinInfo hace un seguimiento de una conexión de pin durante la depuración.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Método CBasePin.DisplayPinInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98930ec48d3daa13d6ae463b38ce1ae62d745de9fae65915dcabcedf3cd673aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916475"
---
# <a name="cbasepindisplaypininfo-method"></a>Método CBasePin.DisplayPinInfo

El `DisplayPinInfo` método hace un seguimiento de una conexión de pin durante la depuración.

## <a name="syntax"></a>Sintaxis


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero al pin receptor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

En las compilaciones de depuración, este método llama a la [**función DbgLog**](dbglog.md) para realizar un seguimiento de un intento de conexión. En las compilaciones comerciales, este método no hace nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




