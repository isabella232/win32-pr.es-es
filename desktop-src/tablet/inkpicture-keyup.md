---
description: Se produce cuando se libera una clave mientras el control InkPicture tiene el foco.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: Evento InkPicture.KeyUp (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e06556f3b4797f04e6b818ea5952d4275bf66467c7d6d0a0bd0e370c6ea12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218426"
---
# <a name="inkpicturekeyup-event"></a>Evento InkPicture.KeyUp

Se produce cuando se libera una clave mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyCode* \[ in, out\]
</dt> <dd>

Valor ASCII de la tecla que se está pulsando.

</dd> <dt>

*Mayús* \[ in, out\]
</dt> <dd>

Estado de la tecla MAYÚS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEKeyUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

