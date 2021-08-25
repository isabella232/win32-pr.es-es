---
description: El método put \_ WindowStyleEx establece los estilos de ventana extendidos.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: CBaseControlWindow.put_WindowStyleEx método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48bdfba6b388d4595af3ba886ed97567c12f080953e238c03d8a5fb36f7a6ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635545"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>Método CBaseControlWindow.put \_ WindowStyleEx

El `put_WindowStyleEx` método establece los estilos de ventana extendidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WindowStyleEx* \[ En\]
</dt> <dd>

Valor que especifica el estilo de la ventana de control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR.

## <a name="remarks"></a>Comentarios

Este método usa estilos de ventana extendidos. Para obtener una lista completa de los estilos de ventana extendidos, consulte la función **CreateWindowEx de** Microsoft Win32. Para cambiar el estilo de la ventana, recupere el estilo de ventana actual y agregue o quite los campos de bits necesarios.

No use los siguientes estilos de ventana porque no están validados.

-   WS \_ DISABLED
-   WS \_ HSCROLL
-   WS \_ ICONIC
-   WS \_ MAXIMIZE
-   WS \_ MINIMIZE
-   WS \_ VSCROLL

Con algunas excepciones (anotadas aquí), las marcas aceptables son las mismas que las permitidas por la función **CreateWindow de** Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




