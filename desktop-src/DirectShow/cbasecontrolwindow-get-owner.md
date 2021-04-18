---
description: El \_ método get Owner recupera el propietario de la ventana actual.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Método CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670888"
---
# <a name="cbasecontrolwindowget_owner-method"></a>CBaseControlWindow. Get \_ Owner (método)

El `get_Owner` método recupera el propietario de la ventana actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propietario* 
</dt> <dd>

Puntero al propietario de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

La ventana de vídeo puede reproducirse en un entorno de documento. Para ello, se debe hacer que la ventana sea un elemento secundario de otra ventana (para que se recorte y se mueva correctamente). Esta propiedad permite establecer y recuperar el propietario de la ventana. Cuando la ventana es propiedad de otra ventana, simplemente llama a la función **SetParent** de Microsoft Win32. Una aplicación que llama a esta función cambiará los estilos de ventana para establecer el \_ bit de WS secundario en.

Cuando la ventana es propiedad de otra ventana, reenvía automáticamente determinados conjuntos de mensajes (en particular, los mensajes del mouse y del teclado). Esto permite que una aplicación realice una edición sencilla de la zona activa y otras interacciones.

Esta función miembro está pensada para que la llamen los objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizar con el filtro asociado. Llame a la función miembro [**CBaseControlWindow:: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) para recuperar esta propiedad si no llama a desde un objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




