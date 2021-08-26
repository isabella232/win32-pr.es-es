---
description: El método GetVideoSize recupera el ancho y el alto del vídeo nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Método CBaseControlVideo.GetVideoSize (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49f58901ac362b5a03d069485ec4dbf74e22d4549dc628f26baa5c2bfa85234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056945"
---
# <a name="cbasecontrolvideogetvideosize-method"></a>Método CBaseControlVideo.GetVideoSize

El método recupera el ancho y el alto del `GetVideoSize` vídeo nativo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntero al ancho del vídeo.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al alto del vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




