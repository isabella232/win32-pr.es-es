---
description: 'El método Stop detiene el objeto. Este método implementa el método IMediaFilter:: stop.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Método CBaseMediaFilter. STOP (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660201"
---
# <a name="cbasemediafilterstop-method"></a>CBaseMediaFilter. STOP (método)

El `Stop` método detiene el objeto. Este método implementa el método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

En la clase base, este método establece la variable miembro de [**\_ Estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) en estado \_ detenido, pero no hace nada más.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




