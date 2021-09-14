---
description: El método OnSize controla los mensajes \_ WM SIZE.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Método CBaseWindow.OnSize (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973917"
---
# <a name="cbasewindowonsize-method"></a>CBaseWindow.OnSize (método)

El `OnSize` método controla los mensajes WM \_ SIZE.

## <a name="syntax"></a>Sintaxis


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Width* 
</dt> <dd>

Ancho del área de cliente, en píxeles.

</dd> <dt>

*Height* 
</dt> <dd>

Alto del área de cliente, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

Este método almacena el nuevo ancho y alto. Para recuperar estos valores, llame a los métodos [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) y [**CBaseWindow::GetWindowWidth.**](cbasewindow-getwindowwidth.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




