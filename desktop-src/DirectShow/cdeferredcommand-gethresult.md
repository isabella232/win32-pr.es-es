---
description: El método GetHResult recupera el valor HRESULT del comando invocado.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Método CDeferredCommand.GetHResult (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061311"
---
# <a name="cdeferredcommandgethresult-method"></a>Método CDeferredCommand.GetHResult

El `GetHResult` método recupera el valor **HRESULT** del comando invocado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phrResult* 
</dt> <dd>

Puntero al **valor HRESULT.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ ABORT si **m \_ pQueue** es **NULL.** De lo contrario, devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IDeferredCommand::GetHResult.**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




