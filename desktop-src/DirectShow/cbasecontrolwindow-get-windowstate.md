---
description: El \_ método get WindowState recupera el estado actual de la ventana.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Método CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671565"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>CBaseControlWindow. Get \_ WindowState (método)

El `get_WindowState` método recupera el estado actual de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWindowState* 
</dt> <dd>

Puntero al estado de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve un subconjunto de los parámetros de la función **ShowWindow** de Microsoft Win32. En concreto, devuelve SW \_ Show y SW \_ Hide, dependiendo de la visibilidad actual de la ventana. También devuelve SW \_ minimizar y SW \_ maximizar, dependiendo de si la ventana es un icono o está expandida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




