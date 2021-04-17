---
description: El \_ método put Owner establece la ventana primaria de la ventana de vídeo; a continuación, la ventana primaria reenvía determinados mensajes a la ventana de vídeo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Método CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661144"
---
# <a name="cbasecontrolwindowput_owner-method"></a>CBaseControlWindow. put ( \_ método de propietario)

El `put_Owner` método establece la ventana primaria de la ventana de vídeo; a continuación, la ventana primaria reenvía determinados mensajes a la ventana de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propietario* 
</dt> <dd>

Identificador de la ventana primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NoError.

## <a name="remarks"></a>Observaciones

Internamente, este método llama a la función **SetParent** de Microsoft Win32 para establecer el nuevo propietario y establece el estilo de la ventana primaria en WS \_ Child. A continuación, la ventana primaria reenvía determinados conjuntos de mensajes (en particular, los mensajes del mouse y del teclado) a la ventana de vídeo.

Después de establecer el propietario de la ventana de vídeo, debe establecer el propietario en **null** y el estilo de ventana del propietario en WS \_ OVERLAPPED y WS \_ CLIPCHILDREN antes de liberar el gráfico de filtro. Cuando se establece el propietario en **null**, este método desactiva el bit de WS secundario de la ventana primaria \_ . Si no establece el propietario en **null**, la ventana primaria seguirá transmitiendo mensajes a la ventana de vídeo y es probable que se produzcan errores cuando se cierre la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




