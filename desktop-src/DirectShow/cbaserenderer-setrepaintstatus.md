---
description: El método SetRepaintStatus habilita o deshabilita los eventos Repaint.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Método CBaseRenderer. SetRepaintStatus (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671673"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>CBaseRenderer. SetRepaintStatus, método

El `SetRepaintStatus` método habilita o deshabilita los eventos Repaint.

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

Valor booleano que indica si están habilitados los eventos Repaint. Si **es true**, el filtro enviará los eventos de [**EC \_ Repaint**](ec-repaint.md) al administrador de gráficos de filtro. De lo contrario, no enviará \_ eventos de Repaint de EC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método garantiza que el administrador de gráficos de filtro no se inunda con eventos de Repaint de EC redundantes \_ . Una vez que el filtro envía un evento [**re \_ Repaint**](ec-repaint.md) , llama a este método con el valor **true**. El filtro no envía más eventos de \_ Repaint de EC hasta que reciba más datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




