---
description: El método SetDrawContext establece los contextos de dispositivo usados para dibujar.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Método CDrawImage.SetDrawContext (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58a10c9f1a485058ed460f4cd30cd4d3894b471415f131d7d4aa59ee757b87d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055975"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Método CDrawImage.SetDrawContext

El `SetDrawContext` método establece los contextos de dispositivo utilizados para dibujar.

## <a name="syntax"></a>Sintaxis


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método recupera los contextos de dispositivo de ventana y memoria del objeto [**CBaseWindow**](cbasewindow.md) propietario. Llame a este método después de inicializar la ventana, pero antes de empezar a dibujar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




