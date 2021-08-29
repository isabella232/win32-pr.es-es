---
description: Se llama al método PrepareRender antes de que el filtro represente un ejemplo.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Método CBaseRenderer.PrepareRender (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3443d3344d24d6f121e2c236b9742a44a97e06414ab264953c29ad004e38d7dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872205"
---
# <a name="cbaserendererpreparerender-method"></a>Método CBaseRenderer.PrepareRender

Se `PrepareRender` llama al método antes de que el filtro represente un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El filtro llama a este método antes de llamar al método [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) o [**al método CBaseRenderer::Render.**](cbaserenderer-render.md) `PrepareRender` no hace nada en la clase base. La clase derivada puede invalidarla para realizar las acciones necesarias antes de la representación. Por ejemplo, un representador de vídeo puede invalidar este método para realizar su paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




