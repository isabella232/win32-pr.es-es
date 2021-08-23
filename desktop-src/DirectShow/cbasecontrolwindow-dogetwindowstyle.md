---
description: El método DoGetWindowStyle recupera los estilos de ventana normales o extendidos actuales.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow.DoGetWindowStyle (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fe158e4a17b898110a2555f87b469ee934aa791b6f0379f9054642810673389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793765"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Método CBaseControlWindow.DoGetWindowStyle

El `DoGetWindowStyle` método recupera los estilos de ventana normales o extendidos actuales.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStyle* 
</dt> <dd>

Puntero a una variable que recibe la información de estilo.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valor que especifica los estilos que se recuperarán. Debe ser una de las siguientes:



| Etiqueta | Value |
|--------------|--------------------------------------|
| ESTILO \_ GWL   | Recupere los estilos de ventana.          |
| GWL \_ EXSTYLE | Recupere los estilos de ventana extendidos. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro llama a la función **GetWindowLong** de Win32 para recuperar el estilo de ventana. Lo llaman las funciones [**miembro CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) y [**CBaseControlWindow::get \_ WindowStyleEx.**](cbasecontrolwindow-get-windowstyleex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




