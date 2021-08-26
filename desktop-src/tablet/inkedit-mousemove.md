---
description: Se produce cuando el usuario mueve el mouse mientras el mouse está sobre el control InkEdit.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: Evento InkEdit.MouseMove (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 601bcaa4c5bc3379c207302c28e5eb17d44b2b184ce42452d5b78b6079d88ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939115"
---
# <a name="inkeditmousemove-event"></a>Evento InkEdit.MouseMove

Se produce cuando el usuario mueve el mouse mientras el mouse está sobre el control [InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MouseMove(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Botón* 
</dt> <dd>

Miembro de la [**enumeración MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica qué botones del mouse están deprimidos.



| Value                                                                                                                                                            | Significado                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**NO \_ BUTTON**</dt> </dl>             | Predeterminada. No se presionó ningún botón del mouse. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**LEFT \_ BUTTON**</dt> </dl>       | Se presionó el botón primario del mouse. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**RIGHT \_ BUTTON**</dt> </dl>    | Se presionó el botón secundario del mouse. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**MIDDLE \_ BUTTON**</dt> </dl> | Se presionó el botón central del mouse. <br/>  |



 

</dd> <dt>

*MayúsKey* 
</dt> <dd>

Miembro de la [**enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica qué teclas modificadoras están deprimidas en el momento del evento.



| Value                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Especifica que la tecla MAYÚS se usó como modificador. <br/> |
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

## <a name="remarks"></a>Comentarios

Si se presiona un botón del mouse mientras el puntero está sobre un control [InkEdit,](inkedit-control-reference.md) ese control captura el mouse y recibe todos los eventos del mouse hasta e incluyendo el último [**evento MouseUp.**](inkedit-mouseup.md) Esto implica que es posible que las coordenadas del puntero del mouse (x, y) devueltas por un evento del mouse no siempre se encontraran en el área interna del objeto que las recibe.

Si los botones del mouse se presionan sucesivamente, el objeto que captura el mouse después de la primera pulsación recibe todos los eventos del mouse hasta que se liberan todos los botones.

El **evento MouseMove** se genera continuamente a medida que el puntero del mouse se mueve entre objetos. A menos que otro objeto haya capturado el mouse, un control [InkEdit](inkedit-control-reference.md) reconoce un evento **MouseMove** cada vez que la posición del mouse está dentro de sus bordes.

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeMouseMove.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada manuscrita)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkMouseButton (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Evento MouseDown \[ InkEdit (control)\]**](inkedit-mousedown.md)
</dt> <dt>

[**MouseUp Event \[ InkEdit (Control)\]**](inkedit-mouseup.md)
</dt> </dl>

 

