---
description: Se produce cuando se suelta una tecla mientras el control InkPicture tiene el foco.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: Evento InkPicture. KeyUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716457"
---
# <a name="inkpicturekeyup-event"></a>InkPicture. KeyUp (evento)

Se produce cuando se suelta una tecla mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.

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

Valor ASCII de la tecla que se va a presionar.

</dd> <dt>

*Desplazamiento* \[ in, out\]
</dt> <dd>

Estado de la tecla Mayús.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEKeyUp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

