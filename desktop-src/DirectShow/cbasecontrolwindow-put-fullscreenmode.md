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
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160207"
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

## <a name="remarks"></a>Observaciones

Un representador de vídeo que implemente un modo de pantalla completa debe invalidar esta función miembro e implementar los modos que admita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




