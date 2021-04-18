---
description: El método SetRealize especifica si la ventana observa las paletas.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Método CBaseWindow. SetRealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681178"
---
# <a name="cbasewindowsetrealize-method"></a>CBaseWindow. SetRealize, método

El `SetRealize` método especifica si la ventana observa las paletas.

## <a name="syntax"></a>Sintaxis


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bRealize* 
</dt> <dd>

Valor booleano que especifica si se deben obtener las paletas. Si **es true**, el método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) obtiene las paletas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el método **SetPalette** obtiene la paleta especificada. Llame a este método para cambiar el comportamiento predeterminado, de modo que las paletas estén seleccionadas pero no se hayan realizado. Este método establece la variable miembro [**CBaseWindow:: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




