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
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061283"
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

## <a name="remarks"></a>Observaciones

Este método recupera los contextos de dispositivo de ventana y memoria del objeto [**CBaseWindow**](cbasewindow.md) propietario. Llame a este método después de inicializar la ventana, pero antes de empezar a dibujar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




