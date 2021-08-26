---
description: El método put \_ FullScreenMode establece el modo de pantalla completa del representador.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: CBaseControlWindow.put_FullScreenMode método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e7aa121ce78198fe6b2ca0b88109183665f0cd93dd95294a848a2b2d0c03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983685"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow.put \_ FullScreenMode (método)

El `put_FullScreenMode` método establece el modo de pantalla completa del representador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Modo de pantalla completa que se aplicará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** La implementación actual devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Comentarios

Un representador de vídeo que implementa un modo de pantalla completa debe invalidar esta función miembro e implementar los modos que admita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




