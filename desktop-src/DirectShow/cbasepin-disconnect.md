---
description: 'Método CBasePin.Disconnect: el método Disconnect interrumpe la conexión de pin actual. Este método implementa el método IPin::D isconnect.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Método CBasePin.Disconnect (Amfilter.h)
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
ms.openlocfilehash: bda01d02db2a93a90c63f206b723a55df2373418
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061357"
---
# <a name="cbasepindisconnect-method"></a>Método CBasePin.Disconnect

El `Disconnect` método interrumpe la conexión de pin actual. Este método implementa el [**método IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                         | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | El pin no estaba conectado.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Correcto.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ NOT \_ STOPPED**</dt> </dl> | El filtro está activo y el pin no admite la reconexión dinámica.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase base delega la mayor parte del trabajo en el método [**CBasePin::D isconnectInternal.**](cbasepin-disconnectinternal.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




