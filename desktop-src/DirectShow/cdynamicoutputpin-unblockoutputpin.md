---
description: El método UnblockOutputPin desbloquea la chincha. Cuando se desbloquea el pin, puede entregar ejemplos, cambiar su formato de salida y volver a conectarse.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Método CDynamicOutputPin.UnblockOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062500"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>Método CDynamicOutputPin.UnblockOutputPin

El `UnblockOutputPin` método desbloquea el pin. Cuando se desbloquea el pin, puede entregar ejemplos, cambiar su formato de salida y volver a conectarse.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El pin ya se ha desbloqueado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




