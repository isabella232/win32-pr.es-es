---
description: El método GetInfo recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y de detenerse. Este método implementa el método IAMStreamControl::GetInfo.
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Método CBaseStreamControl.GetInfo (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96bc59b6dc55d73aa16b08f53f831428ae2d2fb7b181d3bb255b61a323b236a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157222"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>Método CBaseStreamControl.GetInfo

El `GetInfo` método recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y de detenerse. Este método implementa el [**método IAMStreamControl::GetInfo.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* 
</dt> <dd>

Puntero a una [**estructura DE AM STREAM \_ \_ INFO,**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) asignada por el autor de la llamada, que recibe la configuración actual del control de flujo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 




