---
description: El método DoSetWindowStyle cambia el estilo de ventana típico o extendido.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660258"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>CBaseControlWindow. DoSetWindowStyle, método

El `DoSetWindowStyle` método cambia el estilo de ventana típico o extendido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estilo* 
</dt> <dd>

Estilos de ventana adecuados.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valor que especifica los estilos que se van a establecer. Debe ser una de las siguientes:



|              |                                      |
|--------------|--------------------------------------|
| \_estilo GWL   | Recupere los estilos de ventana.          |
| GWL \_ EXstyle | Recupere los estilos extendidos de ventana. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro llama a la función **SetWindowLong** de Win32 para establecer el estilo de ventana y, a continuación, vuelve a mostrar la ventana en la posición actual. Esta función miembro se llama mediante las funciones miembro [**CBaseControlWindow::p UT \_ estiloVentana**](cbasecontrolwindow-put-windowstyle.md) y [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




