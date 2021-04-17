---
description: El método Disconnect interrumpe la conexión del PIN actual. Este método implementa el método IPin::D Ulta.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Método CBasePin. disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671105"
---
# <a name="cbasepindisconnect-method"></a>CBasePin. disconnect (método)

El `Disconnect` método interrumpe la conexión del PIN actual. Este método implementa el método [**IPin::D Ulta**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                         | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | El PIN no estaba conectado.<br/>                                              |
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Correcto.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ no \_ detenido**</dt> </dl> | El filtro está activo y el PIN no admite la reconexión dinámica.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase base delega la mayor parte del trabajo en el método [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




