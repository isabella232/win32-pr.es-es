---
description: El método DoGetWindowStyle recupera los estilos de ventana normales o extendidos actuales.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
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
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670849"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>CBaseControlWindow. DoGetWindowStyle, método

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

Valor que especifica los estilos que se van a recuperar. Debe ser una de las siguientes:



|              |                                      |
|--------------|--------------------------------------|
| \_estilo GWL   | Recupere los estilos de ventana.          |
| GWL \_ EXstyle | Recupere los estilos extendidos de ventana. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro llama a la función **GetWindowLong** de Win32 para recuperar el estilo de ventana. Lo llaman las funciones miembro [**CBaseControlWindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) y [**CBaseControlWindow:: get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




