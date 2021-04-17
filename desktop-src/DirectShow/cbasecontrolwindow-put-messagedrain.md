---
description: El \_ método put MessageDrain establece la ventana para recibir los mensajes de ventana enviados al representador de vídeo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Método CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661146"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>CBaseControlWindow. put \_ MessageDrain (método)

El `put_MessageDrain` método establece la ventana para recibir los mensajes de ventana enviados al representador de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Purga* 
</dt> <dd>

Ventana en la que se van a enviar mensajes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Los mensajes enviados al filtro de representador de vídeo se pueden publicar en otra ventana. Esta función miembro registra la ventana para recibir estos mensajes. A diferencia de la función miembro [**CBaseControlWindow::p UT \_ Owner**](cbasecontrolwindow-put-owner.md) , esta función miembro no hace que la ventana de vídeo sea un elemento secundario de otra ventana. Es especialmente útil para los representadores de vídeo de pantalla completa, que no pueden ser ventanas secundarias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




