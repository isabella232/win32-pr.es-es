---
title: MM_JOY2BUTTONUP mensaje (Mmsystem.h)
description: El mensaje MMMID2BUTTONUP notifica a la ventana que ha capturado el botón DE BOTÓN2 que se ha \_ liberado.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265964"
---
# <a name="mm_joy2buttonup-message"></a>Mensaje \_ MMMIENTO2BUTTONUP

El **mensaje \_ MMIJO2BUTTONUP** notifica a la ventana que ha capturado el botón DE BOTÓN2 que se ha liberado.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

**fwButtons** 
</dt> <dd>

Identifica el botón que ha cambiado el estado y los botones que se presionan. Puede tener uno de los valores siguientes:



| Value                                                                                                                                                            | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**\_BUTTON1CHG DE BUTTON1 DE BUTTON1**</dt> </dl> | El primer botón button ha cambiado de estado.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**\_BUTTON2CHG DE BUTTON2 DE BUTTON2**</dt> </dl> | El segundo botón button ha cambiado de estado.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**\_BUTTON3CHG DE BUTTON3CHG**</dt> </dl> | El tercer botón button ha cambiado de estado.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**\_BUTTON4CHG DE BUTTON4CHG**</dt> </dl> | El cuarto botón button ha cambiado de estado.<br/> |



 

y uno o varios de los siguientes:



| Value                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1**</dt> </dl> | Se presiona el primer botón button button (Botón button).<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**BUTTON2 \_ DE BUTTON2 PARA BUTTON2**</dt> </dl> | Se presiona el segundo botón button button (Segundo botón button).<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**BUTTON3 \_ DE BUTTON3 DE BUTTON3**</dt> </dl> | Se presiona el tercer botón button button (Tercer botón button).<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**BUTTON4 \_ DE BUTTON4 DE BUTTON4**</dt> </dl> | Se presiona el cuarto botón button button (Cuarto botón button).<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

Las coordenadas x del ángulo con respecto a la esquina superior izquierda del área de cliente.

</dd> <dt>

**yPos** 
</dt> <dd>

Coordenada y del ángulo con respecto a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensajes multimedia multimedia](multimedia-joystick-messages.md)
</dt> </dl>

 

 





