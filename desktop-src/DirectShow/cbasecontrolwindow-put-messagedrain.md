---
description: El método put \_ MessageDrain establece la ventana para recibir mensajes de ventana enviados al representador de vídeo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: CBaseControlWindow.put_MessageDrain método (Ctlutil.h)
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
ms.openlocfilehash: b58ac59d83023530ca6da51efc2f84ba42c4bef9ac0d3f25ad9a234a320291f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017263"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>CBaseControlWindow.put \_ MessageDrain (método)

El `put_MessageDrain` método establece la ventana para recibir mensajes de ventana enviados al representador de vídeo.

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

Ventana en la que se publican mensajes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Los mensajes enviados al filtro del representador de vídeo se pueden publicar en otra ventana. Esta función miembro registra la ventana para recibir estos mensajes. A diferencia de la función miembro [**CBaseControlWindow::p ut \_ Owner,**](cbasecontrolwindow-put-owner.md) esta función miembro no convierte la ventana de vídeo en un elemento secundario de otra ventana. Es especialmente útil para los representadores de vídeo de pantalla completa, que no pueden ser ventanas secundarias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




