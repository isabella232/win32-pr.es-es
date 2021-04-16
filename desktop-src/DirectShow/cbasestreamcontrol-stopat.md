---
description: 'El método StopAt informa al pin Cuándo detener la entrega de datos. Este método implementa el método IAMStreamControl:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Método CBaseStreamControl. StopAt (Strmctl. h)
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
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678890"
---
# <a name="cbasestreamcontrolstopat-method"></a>CBaseStreamControl. StopAt, método

El `StopAt` método informa al pin Cuándo detener la entrega de datos. Este método implementa el método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

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

Puntero a un valor de [**\_ hora de referencia**](reference-time.md) que especifica cuando el PIN debe dejar de entregar datos.

</dd> <dt>

*bSendExtra* 
</dt> <dd>

Especifica un valor booleano que indica si se va a enviar un ejemplo adicional después de la hora de detención programada. Si **es true**, el PIN envía un ejemplo adicional.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Especifica un valor que se enviará junto con la notificación de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




