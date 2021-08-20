---
description: El método put \_ AutoShow establece la marca de estado AutoShow.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: CBaseControlWindow.put_AutoShow método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8e24686baa3cf1f2ad570394acd7a290ac374043b8564566dc1e89668d3f6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017283"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>CBaseControlWindow.put \_ AutoShow (método)

El `put_AutoShow` método establece la marca de estado AutoShow.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Autoshow* 
</dt> <dd>

Marca booleana de Automation (0 está desactivada, 1 está desactivada).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta propiedad simplifica el acceso de visualización de ventana para las aplicaciones. Si se establece en 1 (on), la ventana, que normalmente se oculta después de conectar el filtro, se mostrará automáticamente cuando el filtro se pause o se ejecute. Sin embargo, la ventana no debe ocultarse cuando se detiene el filtro. Si se establece en 0 (desactivado), la ventana se hace visible solo cuando la aplicación llama [**a CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




