---
description: El método RemovePalette elimina la paleta lógica existente y llama a CBaseWindow::UnsetPalette en el objeto CBaseWindow.
ms.assetid: fab531b8-8630-43f8-bf08-cd8f24659bef
title: Método CImagePalette.RemovePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.RemovePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0410772203a22655968fba393c707bda790a5a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273100"
---
# <a name="cimagepaletteremovepalette-method"></a>Método CImagePalette.RemovePalette

El método elimina la paleta lógica existente `RemovePalette` y llama a [**CBaseWindow::UnsetPalette**](cbasewindow-unsetpalette.md) en el **objeto CBaseWindow.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemovePalette();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




