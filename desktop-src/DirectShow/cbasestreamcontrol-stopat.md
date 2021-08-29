---
description: El método StopAt informa al pin cuándo dejar de entregar datos. Este método implementa el método IAMStreamControl::StopAt.
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Método CBaseStreamControl.StopAt (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2cab57715a5b34110e8d92d9829f8b9bc6f819af1b5033198451e412f6e2aa21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983385"
---
# <a name="cbasestreamcontrolstopat-method"></a>Método CBaseStreamControl.StopAt

El `StopAt` método informa al pin cuándo dejar de entregar datos. Este método implementa el [**método IAMStreamControl::StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptStop* 
</dt> <dd>

Puntero a un [**valor REFERENCE \_ TIME**](reference-time.md) que especifica cuándo el pin debe dejar de entregar datos.

</dd> <dt>

*bSendExtra* 
</dt> <dd>

Especifica un valor booleano que indica si se debe enviar una muestra adicional después de la hora de detenerse programada. Si **es TRUE,** el pin envía un ejemplo adicional.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Especifica un valor que se enviará junto con la notificación de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 




