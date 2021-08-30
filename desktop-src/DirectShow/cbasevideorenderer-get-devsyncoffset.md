---
description: El método get DevSyncOffset recupera la desviación estándar del tiempo en milisegundos entre el momento en que se debía cada fotograma y el momento en que se representó realmente, para todos los fotogramas desde que se inició el \_ streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: CBaseVideoRenderer.get_DevSyncOffset método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8be41c3c7ae1be598b7c15f033510134cfa46890c904a79b4d979733e0ab6952
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052355"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>CBaseVideoRenderer.get \_ DevSyncOffset (método)

El método recupera la desviación estándar del tiempo en milisegundos entre el momento en que se debía a cada fotograma y el momento en que se representó realmente, para todos los fotogramas desde que se inició `get_DevSyncOffset` el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piDev* 
</dt> <dd>

Puntero a la desviación estándar de la hora como se describió anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IQualProp::get \_ DevSyncOffset.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




