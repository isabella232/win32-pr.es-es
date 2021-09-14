---
description: Se produce cuando se presiona una tecla y se encuentra en la posición de abajo mientras el control InkPicture tiene el foco.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Evento InkPicture.KeyDown (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256586"
---
# <a name="inkpicturekeydown-event"></a>Evento InkPicture.KeyDown

Se produce cuando se presiona una tecla y se encuentra en la posición de abajo mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
void KeyDown(
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

## <a name="remarks"></a>Observaciones

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEKeyDown.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

