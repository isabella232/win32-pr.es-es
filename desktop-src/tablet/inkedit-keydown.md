---
description: Se produce cuando el usuario presiona una tecla mientras el control InkEdit tiene el foco.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Evento InkEdit. KeyDown (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002886"
---
# <a name="inkeditkeydown-event"></a>Evento InkEdit. KeyDown

Se produce cuando el usuario presiona una tecla mientras el control [InkEdit](inkedit-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pKey* 
</dt> <dd>

Código de tecla virtual de la tecla presionada por el usuario.

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Miembro de la enumeración [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , que indica qué teclas modificadoras están presionadas en el momento del evento.



| Value                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Especifica que la tecla Mayús se utilizó como modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Control** de</dt> </dl> | Especifica que la tecla CTRL se utilizó como modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que la tecla ALT se ha utilizado como modificador. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método de evento se define en la interfaz **\_ IInkEditEvents** . La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyDown.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Control InkEdit de eventos KeyPress \[\]**](inkedit-keypress.md)
</dt> <dt>

[**Control InkEdit de evento KeyUp \[\]**](inkedit-keyup.md)
</dt> </dl>

 

