---
description: El método AlignDown trunca un valor a un límite de alineación especificado.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Método CPullPin.AlignDown (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdf16f3759bb7637fa243ce98bc4886b65e31d25bf62f5e9f581064d3741ea1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585355"
---
# <a name="cpullpinaligndown-method"></a>CPullPin.AlignDown (método)

El `AlignDown` método trunca un valor a un límite de alineación especificado.

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ll* 
</dt> <dd>

Especifica el número que se debe alinear.

</dd> <dt>

*lAlign* 
</dt> <dd>

Especifica el límite de alineación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el resultado alineado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




