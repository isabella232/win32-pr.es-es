---
description: Pasa un mensaje EC \_ VIDEO SIZE CHANGED al administrador de \_ \_ gráficos de filtros.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Método CBaseControlVideo.OnVideoSizeChange (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 689f6f14426d88270136d6cc3687f9e214b72d6e42e2af44f3d189510d61f327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076695"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>Método CBaseControlVideo.OnVideoSizeChange

Pasa un mensaje EC \_ VIDEO SIZE CHANGED al administrador de \_ \_ gráficos de filtros.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que depende de la implementación; puede ser uno de los siguientes valores u otros valores no enumerados.



| Código devuelto                                                                                   | Descripción               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/> |



 

## <a name="remarks"></a>Comentarios

Un representador de vídeo debe llamar a esta función miembro cada vez que se cambia el tamaño del vídeo. Normalmente, se llamará a este método una vez después de la conexión inicial. Si el representador puede admitir cambios de formato dinámico (de 320 x 240 a 160 x 120), también debe llamarlo después de cada cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




