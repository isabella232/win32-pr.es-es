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
ms.openlocfilehash: 819f279d20192ff82d9021e03780713f714682abf47aaf854b4568312572e8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526544"
---
# <a name="cbaserenderersetabortsignal-method"></a>Método CBaseRenderer.SetAbortSignal

El método establece una marca que indica si se `SetAbortSignal` debe detener la representación y rechazar más muestras.

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

Valor booleano que indica si se debe detener la representación. Si **es TRUE,** el filtro no representará más ejemplos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

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

 

 




