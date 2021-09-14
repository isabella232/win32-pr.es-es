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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974040"
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

## <a name="remarks"></a>Observaciones

Esta función miembro llama a la función **GetWindowLong** de Win32 para recuperar el estilo de ventana. Lo llaman las funciones [**miembro CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) y [**CBaseControlWindow::get \_ WindowStyleEx.**](cbasecontrolwindow-get-windowstyleex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




