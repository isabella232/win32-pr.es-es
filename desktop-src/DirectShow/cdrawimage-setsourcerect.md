---
description: El método SetSourceRect establece el rectángulo de origen.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Método CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670508"
---
# <a name="cdrawimagesetsourcerect-method"></a>CDrawImage. SetSourceRect, método

El `SetSourceRect` método establece el rectángulo de origen.

## <a name="syntax"></a>Sintaxis


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntero a una estructura **Rect** que define el nuevo rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método si cambia el rectángulo de origen; por ejemplo, en respuesta a una llamada a [**IBasicVideo:: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .

Valide el rectángulo proporcionado en *pSourceRect* antes de llamar a este método para asegurarse de que no se extiende más allá del tamaño de vídeo nativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




