---
description: El método OnClose controla \_ los mensajes de cierre de WM.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Método CBaseWindow. OnClose (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660317"
---
# <a name="cbasewindowonclose-method"></a>CBaseWindow. OnClose (método)

El `OnClose` método controla \_ los mensajes de cierre de WM.

## <a name="syntax"></a>Sintaxis


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="remarks"></a>Observaciones

En la clase base, este método simplemente oculta la ventana. Normalmente, una clase derivada invalidará este método para que envíe también un evento [**\_ USERABORT de EC**](ec-userabort.md) . No invalide el método para destruir la ventana. En su lugar, llame al método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) cuando se destruya el filtro propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




