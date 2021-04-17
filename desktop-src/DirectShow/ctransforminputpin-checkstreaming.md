---
description: El método CheckStreaming determina si el pin puede aceptar ejemplos.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Método CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660686"
---
# <a name="ctransforminputpincheckstreaming-method"></a>CTransformInputPin. CheckStreaming, método

El `CheckStreaming` método determina si el pin puede aceptar ejemplos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | El PIN se está vaciando actualmente.<br/>       |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN de salida no está conectado.<br/> |
| <dl> <dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt> </dl> | Se produjo un error en tiempo de ejecución.<br/>       |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl>   | El PIN está detenido.<br/>              |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




