---
description: El método SetSourceRect establece el rectángulo de origen.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Método CDrawImage.SetSourceRect (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061282"
---
# <a name="cdrawimagesetsourcerect-method"></a>Método CDrawImage.SetSourceRect

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

Puntero a una **estructura RECT** que define el nuevo rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método si cambia el rectángulo de origen; por ejemplo, en respuesta a una [**llamada a IBasicVideo::SetSourcePosition.**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition)

Valide el rectángulo especificado en *pSourceRect antes* de llamar a este método para asegurarse de que no se extiende más allá del tamaño de vídeo nativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




