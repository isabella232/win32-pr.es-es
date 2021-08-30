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
ms.openlocfilehash: 16513cd202d8ad1973a6aa4d2bfd69f8372cb9b611e1dc070e265685db2d2682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910105"
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

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IDeferredCommand::GetHResult.**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




