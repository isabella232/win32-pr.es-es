---
description: El método GetDefaultRect recupera el tamaño predeterminado del área de cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Método CBaseWindow.GetDefaultRect (Winutil.h)
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
ms.openlocfilehash: e64d13a3fe77370d4b5bbefb7d493738b035c40ceebd13cd7f6f0f5c6d03f783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074619"
---
# <a name="cbasewindowgetdefaultrect-method"></a>Método CBaseWindow.GetDefaultRect

El `GetDefaultRect` método recupera el tamaño predeterminado del área de cliente.

## <a name="syntax"></a>Sintaxis


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el rectángulo predeterminado.

## <a name="remarks"></a>Comentarios

Cuando se activa la ventana, el objeto llama a este método para determinar el tamaño que debe tener el área de cliente de la ventana. En la clase base, este método devuelve un rectángulo cuyo alto y ancho son las constantes definidas DEFHEIGHT y DEFWIDTH. Una clase derivada debe invalidar este método. Para un representador de vídeo, la clase derivada normalmente devolverá el tamaño de la imagen de vídeo nativa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




