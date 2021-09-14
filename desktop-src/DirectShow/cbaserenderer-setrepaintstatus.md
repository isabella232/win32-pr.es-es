---
description: El método SetRepaintStatus habilita o deshabilita los eventos de repintado.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Método CBaseRenderer.SetRepaintStatus (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061764"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Método CBaseRenderer.SetRepaintStatus

El `SetRepaintStatus` método habilita o deshabilita los eventos de repintado.

## <a name="syntax"></a>Sintaxis


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bRepaint* 
</dt> <dd>

Valor booleano que indica si los eventos de repintado están habilitados. Si **es TRUE,** el filtro enviará eventos [**EC \_ REPAINT**](ec-repaint.md) al administrador de gráficos de filtros. De lo contrario, no enviará eventos \_ EC REPAINT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método garantiza que el administrador de gráficos de filtro no se inunde con eventos \_ EC REPAINT redundantes. Una vez que el filtro envía [**un evento EC \_ REPAINT,**](ec-repaint.md) llama a este método con el valor **TRUE**. El filtro no envía más eventos \_ EC REPAINT hasta que recibe más datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




