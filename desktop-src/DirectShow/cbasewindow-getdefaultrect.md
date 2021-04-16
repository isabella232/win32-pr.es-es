---
description: El método GetDefaultRect recupera el tamaño predeterminado del área cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Método CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679568"
---
# <a name="cbasewindowgetdefaultrect-method"></a>CBaseWindow. GetDefaultRect, método

El `GetDefaultRect` método recupera el tamaño predeterminado del área cliente.

## <a name="syntax"></a>Sintaxis


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el rectángulo predeterminado.

## <a name="remarks"></a>Observaciones

Cuando se activa la ventana, el objeto llama a este método para determinar el tamaño que debe tener el área cliente de la ventana. En la clase base, este método devuelve un rectángulo cuyo alto y ancho son las constantes definidas DEFHEIGHT y DEFWIDTH. Una clase derivada debe reemplazar este método. En el caso de un representador de vídeo, la clase derivada normalmente devolverá el tamaño de la imagen de vídeo nativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




