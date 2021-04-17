---
description: 'El método WaitForReceiveToComplete espera a que se complete el método CBaseRenderer:: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Método CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670343"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>CBaseRenderer. WaitForReceiveToComplete, método

El `WaitForReceiveToComplete` método espera a que se complete el método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .

## <a name="syntax"></a>Sintaxis


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) y [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) llaman a este método para sincronizar el cambio de estado con el método **Receive** .

En concreto, este método envía los mensajes mientras espera a que la marca [**CBaseRenderer:: m \_ bInReceive**](cbaserenderer-m-binreceive.md) se convierta en **false**. La marca se convierte en **true** en el método [**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md) y vuelve a cambiar a **false** después de que el método **Receive** llame al método [**CBaseRenderer::P reparerender**](cbaserenderer-preparerender.md) . La clase derivada puede usar **PrepareRender** para establecer la paleta. Esperar a que se complete **PrepareRender** se asegura de que los mensajes de cambio de paleta se envíen antes de que se produzca el cambio de estado. Esto evita un posible interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




