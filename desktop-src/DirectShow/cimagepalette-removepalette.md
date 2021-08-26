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
ms.openlocfilehash: 0b87c8f028da17e6af305900f203c5cf1143132806ca1b2ce9b0edaddebd0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916015"
---
# <a name="cimagepaletteremovepalette-method"></a>CImagePalette.RemovePalette (método)

El método elimina la paleta lógica existente `RemovePalette` y llama [**a CBaseWindow::UnsetPalette**](cbasewindow-unsetpalette.md) en el **objeto CBaseWindow.**

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




