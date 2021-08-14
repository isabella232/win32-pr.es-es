---
description: Se produce cuando el puntero del mouse sale del control InkPicture.
ms.assetid: 4b7961cd-58a3-4e75-bb9e-fbb6dc225d3d
title: Evento InkPicture.MouseLeave (Ms mouseut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff08c3ffbac12911d5eda02a67da2bd31213f943a14afe77f5e7fc17ca885933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218386"
---
# <a name="inkpicturemouseleave-event"></a>Evento InkPicture.MouseLeave

Se produce cuando el puntero del mouse sale del control [InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void MouseLeave();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEMouseLeave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

