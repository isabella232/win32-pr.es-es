---
description: El método \_ get BackgroundPalette recupera la paleta realizada en la marca de fondo.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: CBaseControlWindow.get_BackgroundPalette método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974038"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>Método CBaseControlWindow.get \_ BackgroundPalette

El `get_BackgroundPalette` método recupera la paleta realizada en la marca de fondo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

Puntero a una marca booleana de Automation (0 está desactivado, 1 está on).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IVideoWindow::get \_ BackgroundPalette.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) Si se reproduce un vídeo dentro de otra aplicación o documento, es posible que la aplicación quiera usar su propia paleta. Puede pedir que el vídeo use la paleta de primer plano actual en lugar de la suya propia estableciendo esta marca en 1. Si se establece en 0, la ventana se instalará y se dará cuenta de su propia paleta preferida. Tenga en cuenta que pedir a la ventana que use una paleta diferente provocará graves penalizaciones de rendimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




