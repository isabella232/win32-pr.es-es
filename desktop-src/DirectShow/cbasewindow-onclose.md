---
description: El método OnClose controla los mensajes WM \_ CLOSE.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Método CBaseWindow.OnClose (Winutil.h)
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
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635145"
---
# <a name="cbasewindowonclose-method"></a>CBaseWindow.OnClose (método)

El `OnClose` método controla los mensajes WM \_ CLOSE.

## <a name="syntax"></a>Sintaxis


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

En la clase base, este método simplemente oculta la ventana. Normalmente, una clase derivada invalidará este método para que envíe también un evento [**\_ USERABORT**](ec-userabort.md) de EC. No invalide el método para destruir la ventana. En su lugar, [**llame al método CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) cuando se destruya el filtro propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




