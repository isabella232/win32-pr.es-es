---
description: El método SetWindowPosition establece la posición de la ventana en el escritorio.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Método CBaseControlWindow.SetWindowPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361411"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>Método CBaseControlWindow.SetWindowPosition

El `SetWindowPosition` método establece la posición de la ventana en el escritorio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Left* 
</dt> <dd>

Nueva coordenada izquierda.

</dd> <dt>

*Top* (Principales) 
</dt> <dd>

Nueva coordenada superior.

</dd> <dt>

*Width* 
</dt> <dd>

Ancho de la ventana.

</dd> <dt>

*Height* 
</dt> <dd>

Alto de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




