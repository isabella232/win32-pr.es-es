---
description: El \_ método put WindowStyleEx establece los estilos extendidos de ventana.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Método CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
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
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661339"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>CBaseControlWindow. put \_ WindowStyleEx (método)

El `put_WindowStyleEx` método establece los estilos extendidos de ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WindowStyleEx* \[ de\]
</dt> <dd>

Valor que especifica el estilo de la ventana de control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NoError.

## <a name="remarks"></a>Observaciones

Este método usa estilos extendidos de ventana. Para obtener una lista completa de los estilos de ventana extendidos, vea la función **CreateWindowEx** de Microsoft Win32. Para cambiar el estilo de ventana, recupere el estilo de ventana actual y, a continuación, agregue o quite los campos de bits necesarios.

No utilice los siguientes estilos de ventana porque no se validan.

-   WS \_ deshabilitado
-   WS \_ HSCROLL
-   iconos de WS \_
-   \_maximizar WS
-   \_minimizar WS
-   WS \_ VSCROLL

Con algunas excepciones (que se indican aquí), las marcas aceptables son las mismas que las permitidas por la función **CreateWindow** de Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




