---
description: Se produce cuando el usuario suelta un botón del mouse mientras el mouse está sobre el control InkEdit.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: Evento InkEdit.MouseUp (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c331ec5dd0dd6a39ec956eda6980ee02cddd298e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360290"
---
# <a name="inkeditmouseup-event"></a>Evento InkEdit.MouseUp

Se produce cuando el usuario suelta un botón del mouse mientras el mouse está sobre el control [InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MouseUp(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Button* 
</dt> <dd>

Miembro de la [**enumeración MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica qué botones del mouse se liberaron.



| Value                                                                                                                                                            | Significado                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**NO \_ BUTTON**</dt> </dl>             | Predeterminada. No se presionó ningún botón del mouse. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**LEFT \_ BUTTON**</dt> </dl>       | Se presionó el botón primario del mouse. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**RIGHT \_ BUTTON**</dt> </dl>    | Se presionó el botón secundario del mouse. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**MIDDLE \_ BUTTON**</dt> </dl> | Se presionó el botón central del mouse. <br/>  |



 

</dd> <dt>

*MayúsKey* 
</dt> <dd>

Miembro de la [**enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica qué teclas modificadoras se deprimen en el momento del evento.



| Value                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Desplazamiento \_ de IKM**</dt> </dl>             | Especifica que la tecla MAYÚS se usó como modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Control**</dt> </dl> | Especifica que la tecla CTRL se usó como modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que la tecla ALT se usó como modificador. <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

Coordenada x actual, en píxeles, del puntero del mouse.

</dd> <dt>

*yMouse* 
</dt> <dd>

Coordenada y actual, en píxeles, del puntero del mouse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si se presiona un botón del mouse mientras el puntero está sobre un control [InkEdit,](inkedit-control-reference.md) ese control captura el mouse y recibe todos los eventos del mouse hasta el último evento **MouseUp,** incluido el último. Esto implica que es posible que las coordenadas del puntero del mouse (x, y) devueltas por un evento del mouse no siempre se encontraran en el área interna del objeto que las recibe.

Si los botones del mouse se presionan en sucesión, el objeto que captura el mouse después de la primera pulsación recibe todos los eventos del mouse hasta que se liberan todos los botones.

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeMouseUp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkMouseButton (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Evento MouseDown \[ InkEdit (Control)\]**](inkedit-mousedown.md)
</dt> <dt>

[**MouseMove Event \[ InkEdit Control\]**](inkedit-mousemove.md)
</dt> </dl>

 

