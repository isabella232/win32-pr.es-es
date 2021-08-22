---
title: MM_JOY2BUTTONUP mensaje (Mmsystem.h)
description: El mensaje MM MMMM2BUTTONUP notifica a la ventana que ha capturado la captura de UNID2 que se ha liberado \_ un botón.
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
ms.openlocfilehash: 8f94a1761686bd2e3ac7c470268427a213d54cdb4b8a58d54fdd6961427c2377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557315"
---
# <a name="mm_joy2buttonup-message"></a>Mensaje \_ MM MMMIENTO2BUTTONUP

El **mensaje \_ MMIJO2BUTTONUP** notifica a la ventana que ha capturado la captura de UNID2 que se ha liberado un botón.


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

Identifica el botón que ha cambiado de estado y los botones que se presionan. Puede tener uno de los valores siguientes:



| Valor                                                                                                                                                            | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**\_BUTTON1CHG DE BUTTON1 DE BUTTON**</dt> </dl> | El primer botón button button ha cambiado de estado.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**\_BUTTON2CHG DE BUTTON2 BUTTON2**</dt> </dl> | El segundo botón button button ha cambiado de estado.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**\_BUTTON3CHG DE BUTTON3CHG**</dt> </dl> | El tercer botón button button ha cambiado de estado.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**\_BUTTON4CHG DE BUTTON4CHG**</dt> </dl> | El cuarto botón button button ha cambiado de estado.<br/> |



 

y uno o varios de los siguientes:



| Valor                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1**</dt> </dl> | Se presiona el primer botón de botones.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**BOTÓN \_ BUTTON2 DE BUTTON2**</dt> </dl> | Se presiona el segundo botón button button (Botón de botones).<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**BOTÓN \_ BUTTON3 DE BUTTON3**</dt> </dl> | Se presiona el tercer botón de botones.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**BUTTON4 \_ DE BUTTON4 DE BUTTON**</dt> </dl> | Se presiona el cuarto botón button button (Cuarto botón de botones).<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

Coordenadas x del borde con respecto a la esquina superior izquierda del área cliente.

</dd> <dt>

**yPos** 
</dt> <dd>

Coordenada y del borde con respecto a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensajes multimedia multimedia](multimedia-joystick-messages.md)
</dt> </dl>

 

 





