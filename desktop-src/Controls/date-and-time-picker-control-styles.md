---
title: Estilos de control selector de fecha y hora (CommCtrl.h)
description: Los estilos de ventana enumerados aquí son específicos de los controles de selector de fecha y hora.
ms.assetid: d3b95521-75ef-4cca-b801-94c6f749aa47
topic_type:
- apiref
api_name:
- DTS_APPCANPARSE
- DTS_LONGDATEFORMAT
- DTS_RIGHTALIGN
- DTS_SHOWNONE
- DTS_SHORTDATEFORMAT
- DTS_SHORTDATECENTURYFORMAT
- DTS_TIMEFORMAT
- DTS_UPDOWN
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d24e7543e4e843fc70e0ccacdab670e18e46cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174170"
---
# <a name="date-and-time-picker-control-styles"></a>Estilos de control selector de fecha y hora

Los estilos de ventana enumerados aquí son específicos de los controles de selector de fecha y hora.



| Constante                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**DTS \_ APPCANPARSE**</dt> </dl>                                  | Permite que el propietario analice la entrada del usuario y tome las medidas necesarias. Permite a los usuarios editar dentro del área de cliente del control cuando presionan la tecla F2. El control envía códigos [de notificación \_ DE DTN USERSTRING](dtn-userstring.md) cuando finalizan los usuarios.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**DTS \_ LONGDATEFORMAT**</dt> </dl>                         | Muestra la fecha en formato largo. La cadena de formato predeterminada para este estilo se define mediante LOCALE SLONGDATEFORMAT, que genera una salida como \_ "Friday, April 19, 19, 1996". Cuando se usa este estilo, el botón desplegable no muestra un icono.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**DTS \_ RIGHTALIGN**</dt> </dl>                                     | El calendario del mes desplegable se alineará a la derecha con el control en lugar de alineado a la izquierda, que es el valor predeterminado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**DTS \_ SHOWNONE**</dt> </dl>                                           | Es posible no tener ninguna fecha seleccionada actualmente en el control . Con este estilo, el control muestra una casilla que se selecciona automáticamente cada vez que se selecciona o se introduce una fecha. Si la casilla se deselecciona posteriormente, la aplicación no puede recuperar la fecha del control porque, básicamente, el control no tiene ninguna fecha. El estado de la casilla se puede establecer con el mensaje [**\_ SETSYSTEMTIME**](dtm-setsystemtime.md) de DTM o consultarse con el mensaje [**\_ GETSYSTEMTIME de DTM.**](dtm-getsystemtime.md)<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**DTS \_ SHORTDATEFORMAT**</dt> </dl>                      | Muestra la fecha en formato corto. La cadena de formato predeterminada para este estilo se define mediante LOCALE SSHORTDATE, que genera una salida como \_ "4/19/96".<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**DTS \_ SHORTDATECENTURYFORMAT**</dt> </dl> | **Versión 5.80.** Similar al estilo **\_ SHORTDATEFORMAT de DTS,** salvo que el año es un campo de cuatro dígitos. La cadena de formato predeterminada para este estilo se basa en LOCALE \_ SSHORTDATE. La salida tiene el siguiente aspecto: "19/4/1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**DTS \_ TIMEFORMAT**</dt> </dl>                                     | Muestra la hora. La cadena de formato predeterminada para este estilo se define mediante LOCALE STIMEFORMAT, que genera una salida como \_ "5:31:42 PM".<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**DTS \_ UPDOWN**</dt> </dl>                                                 | Coloca un control de arriba a la derecha del control DTP para modificar los valores de fecha y hora. Este estilo se puede usar en lugar del calendario de mes desplegable, que es el estilo predeterminado.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Observaciones

Los estilos \_ XXXFORMAT de DTS que definen el formato de presentación no se pueden combinar. Si ninguno de los estilos de formato es adecuado, use un [**mensaje \_ SETFORMAT de DTM**](dtm-setformat.md) para definir un formato personalizado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





