---
description: Se produce cuando se presiona una tecla mientras el control InkPicture tiene el foco.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Evento InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001258"
---
# <a name="inkpicturekeypress-event"></a>Evento InkPicture. KeyPress

Se produce cuando se presiona una tecla mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyAscii* \[ in, out\]
</dt> <dd>

Valor ASCII de la tecla que se va a presionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEKeyPress.

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

 

