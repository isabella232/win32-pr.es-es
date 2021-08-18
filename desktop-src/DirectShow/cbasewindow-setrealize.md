---
description: El método SetRealize especifica si la ventana realiza paletas.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Método CBaseWindow.SetRealize (Winutil.h)
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
ms.openlocfilehash: 825a020b73bc74b38a32daa6f6870b76a009f5b8090e253370c77dfce7d7dc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954574"
---
# <a name="cbasewindowsetrealize-method"></a>Método CBaseWindow.SetRealize

El `SetRealize` método especifica si la ventana realiza paletas.

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

Valor booleano que especifica si se deben realizar paletas. Si **es TRUE,** [**el método CBaseWindow::SetPalette**](cbasewindow-setpalette.md) realiza paletas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

De forma predeterminada, **el método SetPalette** realiza la paleta especificada. Llame a este método para cambiar el comportamiento predeterminado, de modo que las paletas se seleccionan pero no se realizan. Este método establece la [**variable miembro CBaseWindow::m \_ bNoRealize.**](cbasewindow-m-bnorealize.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




