---
description: El \_ método visible Put hace que muestre u oculte la ventana.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Método CBaseControlWindow.put_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661344"
---
# <a name="cbasecontrolwindowput_visible-method"></a>CBaseControlWindow. put ( \_ método visible)

El `put_Visible` método hace que muestre u oculte la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Visible* 
</dt> <dd>

Marca booleana de Automation (0 significa que la ventana está oculta; se muestra una ventana de 1).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




