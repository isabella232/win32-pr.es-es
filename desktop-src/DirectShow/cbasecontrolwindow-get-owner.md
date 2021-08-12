---
description: El método get \_ Owner recupera el propietario de la ventana actual.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: CBaseControlWindow.get_Owner método (Ctlutil.h)
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
ms.openlocfilehash: 3a64325fddebc410c5a75a5c2fb8811241012feb6a046b9059897f9b13e0206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660518"
---
# <a name="cbasecontrolwindowget_owner-method"></a>Método CBaseControlWindow.get \_ Owner

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

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

La ventana de vídeo puede reproducirse dentro de un entorno de documento. Para ello, la ventana debe ser un elemento secundario de otra ventana (para que se recorte y se mueve correctamente). Esta propiedad permite establecer y recuperar el propietario de la ventana. Cuando la ventana pertenece a otra ventana, simplemente llama a la función **SetParent** de Microsoft Win32. Una aplicación que llame a esta función cambiará los estilos de ventana para establecer el \_ bit CHILD de WS.

Cuando la ventana es propiedad de otra ventana, reenviará automáticamente determinados conjuntos de mensajes (en particular, mensajes del mouse y del teclado). Esto permite que una aplicación realice una edición de acceso en caliente simple y otras interacciones.

Esta función miembro está pensada para que la llamen objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizarse con el filtro asociado. Llame a [**la función miembro CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) para recuperar esta propiedad si no llama a desde un objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




