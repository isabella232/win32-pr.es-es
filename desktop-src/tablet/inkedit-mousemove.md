---
description: Se produce cuando el usuario mueve el mouse mientras el mouse está sobre el control InkEdit.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: Evento InkEdit. MouseMove (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0d3e98827a1f0ebcdc80f5d44765ebe768f65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648472"
---
# <a name="inkeditmousemove-event"></a>Evento InkEdit. MouseMove

Se produce cuando el usuario mueve el mouse mientras el mouse está sobre el control [InkEdit](inkedit-control-reference.md) .

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

Miembro de la enumeración [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica qué botones del mouse están presionados.



| Value                                                                                                                                                            | Significado                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**No \_ BOTÓN** de</dt> </dl>             | Predeterminada. No se presionó ningún botón del mouse. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**Izquierda \_ BOTÓN** de</dt> </dl>       | Se presionó el botón primario del mouse. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**Derecha \_ BOTÓN** de</dt> </dl>    | Se presionó el botón secundario del mouse. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**Centro \_ BOTÓN** de</dt> </dl> | Se presionó el botón central del mouse. <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Miembro de la enumeración [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica qué teclas modificadoras están presionadas en el momento del evento.



| Value                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Especifica que la tecla Mayús se utilizó como modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Control** de</dt> </dl> | Especifica que la tecla CTRL se utilizó como modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que la tecla ALT se ha utilizado como modificador. <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

Coordenada x actual, en píxeles, del puntero del mouse.

</dd> <dt>

*yMouse* 
</dt> <dd>

La coordenada y actual, en píxeles, del puntero del mouse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si se presiona un botón del mouse mientras el puntero se encuentra sobre un control [InkEdit](inkedit-control-reference.md) , ese control captura el mouse y recibe todos los eventos del mouse hasta el último evento [**MouseUp**](inkedit-mouseup.md) incluido. Esto implica que las coordenadas del puntero del mouse (x, y) devueltas por un evento del mouse pueden no estar siempre en el área interna del objeto que los recibe.

Si los botones del mouse se presionan sucesivamente, el objeto que captura el mouse después de la primera pulsada recibe todos los eventos del mouse hasta que se liberen todos los botones.

El evento **MouseMove** se genera continuamente a medida que el puntero del mouse se mueve por los objetos. A menos que otro objeto haya capturado el mouse, un control [InkEdit](inkedit-control-reference.md) reconoce un evento **MouseMove** siempre que la posición del mouse está dentro de los bordes.

Este método de evento se define en la interfaz **\_ IInkEditEvents** . La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeMouseMove.

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

[**Enumeración InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Control InkEdit de eventos MouseDown \[\]**](inkedit-mousedown.md)
</dt> <dt>

[**Control InkEdit de evento MouseUp \[\]**](inkedit-mouseup.md)
</dt> </dl>

 

