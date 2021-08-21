---
description: El método HideCursor oculta o muestra el cursor.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Método CBaseControlWindow.HideCursor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6421a650471d0954031433db3814e8453cbc82586c7f37608ae947e7301c6969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158386"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>CBaseControlWindow.HideCursor (método)

El `HideCursor` método oculta o muestra el cursor.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HideCursor* 
</dt> <dd>

Valor que especifica si se va a mostrar el cursor. Establezca en OATRUE para ocultar el cursor o en OAFALSE para mostrar el cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




