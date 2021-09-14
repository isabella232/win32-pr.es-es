---
description: El método SetAbortSignal establece una marca que indica si se debe detener la representación y rechazar más ejemplos.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Método CBaseRenderer.SetAbortSignal (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254450"
---
# <a name="cbaserenderersetabortsignal-method"></a>Método CBaseRenderer.SetAbortSignal

El `SetAbortSignal` método establece una marca que indica si se debe detener la representación y rechazar más muestras.

## <a name="syntax"></a>Sintaxis


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bAbort* 
</dt> <dd>

Valor booleano que indica si se va a detener la representación. Si **es TRUE,** el filtro no representará más ejemplos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método establece la [**marca CBaseRenderer::m \_ bAbort.**](cbaserenderer-m-babort.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




