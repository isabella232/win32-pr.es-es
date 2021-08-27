---
description: El método Receive recibe el siguiente ejemplo multimedia en la secuencia.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Método CBaseRenderer.Receive (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe440b7ac0c7b05c2d3cf9d7ca2019a788e272b7aca6acd6a747738a255ca39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131445"
---
# <a name="cbaserendererreceive-method"></a>Método CBaseRenderer.Receive

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

El pin de entrada llama a este método cuando recibe una muestra del filtro ascendente.

Si el filtro se está ejecutando, este método realiza los pasos siguientes:

1.  Programa el ejemplo para la representación ([**CBaseRenderer::P repareReceive**](cbaserenderer-preparereceive.md)).
2.  Espera la hora programada ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Representa el ejemplo ([**CBaseRenderer::Render**](cbaserenderer-render.md)).
4.  Libera el ejemplo ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Si el filtro está en pausa, el método realiza los pasos siguientes:

1.  Notifica a la clase derivada que hay disponible un ejemplo ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Espera a la hora programada.
3.  Representa el ejemplo.
4.  Libera el ejemplo.

Mientras está en pausa, el método espera en el paso 2 hasta que el filtro cambia a un estado de ejecución. En ese momento, el filtro programa el ejemplo.

En la clase base, el **método OnReceiveFirstSample** no hace nada. La clase derivada puede invalidarla. Por ejemplo, cuando un representador de vídeo está en pausa, muestra el primer ejemplo como una imagen fija.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




