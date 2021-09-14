---
description: El método SetControlVideoPin establece el pin utilizado por el filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Método CBaseControlVideo.SetControlVideoPin (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172014"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>Método CBaseControlVideo.SetControlVideoPin

El `SetControlVideoPin` método establece el pin utilizado por el filtro.

## <a name="syntax"></a>Sintaxis


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero al pin con el que se sincroniza la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Solo se puede llamar a la interfaz cuando el filtro se ha conectado correctamente. El objeto se pasa a través de este método al pin con el que está sincronizado; En la mayoría de los casos, determinará si el pin está conectado cuando tiene un método de interfaz llamado y devolverá VFW E NOT CONNECTED si \_ \_ se produce un \_ error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




