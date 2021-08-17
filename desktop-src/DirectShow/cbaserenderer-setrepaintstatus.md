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
ms.openlocfilehash: 748d0091bd3d2eae11773a9f94b62ceeb92b2d3ca64049f1a1981e38bf222e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016853"
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

## <a name="remarks"></a>Comentarios

Este método garantiza que el administrador de gráficos de filtro no se inunde con eventos \_ EC REPAINT redundantes. Una vez que el filtro envía [**un evento EC \_ REPAINT,**](ec-repaint.md) llama a este método con el valor **TRUE**. El filtro no envía más eventos \_ EC REPAINT hasta que recibe más datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




