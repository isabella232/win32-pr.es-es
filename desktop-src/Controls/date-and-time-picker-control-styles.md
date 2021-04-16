---
title: Estilos de control del selector de fecha y hora (CommCtrl. h)
description: Los estilos de ventana que se enumeran aquí son específicos de los controles de selector de fecha y hora.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649722"
---
# <a name="date-and-time-picker-control-styles"></a>Estilos de control de selector de fecha y hora

Los estilos de ventana que se enumeran aquí son específicos de los controles de selector de fecha y hora.



| Constante                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**\_APPCANPARSE DTS**</dt> </dl>                                  | Permite al propietario analizar los datos proporcionados por el usuario y tomar las medidas necesarias. Permite a los usuarios editar dentro del área cliente del control cuando presionan la tecla F2. El control envía códigos de notificación de [DTN \_ USERSTRING](dtn-userstring.md) cuando finalizan los usuarios.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**\_LONGDATEFORMAT DTS**</dt> </dl>                         | Muestra la fecha en formato largo. La cadena de formato predeterminada para este estilo se define mediante la configuración regional \_ SLONGDATEFORMAT, que produce una salida como "Friday, 19 de abril de 1996". Cuando se usa este estilo, el botón desplegable no muestra ningún icono.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**\_RIGHTALIGN DTS**</dt> </dl>                                     | El calendario del mes desplegable se alineará a la derecha con el control en lugar de alinear a la izquierda, que es el valor predeterminado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**\_SHOWNONE DTS**</dt> </dl>                                           | Es posible que no haya ninguna fecha seleccionada actualmente en el control. Con este estilo, el control muestra una casilla que se selecciona automáticamente cada vez que se selecciona o se escribe una fecha. Si la casilla está desactivada posteriormente, la aplicación no puede recuperar la fecha del control porque, en esencia, el control no tiene fecha. El estado de la casilla se puede establecer con el mensaje [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) o consultarlo con el mensaje [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md) .<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**\_SHORTDATEFORMAT DTS**</dt> </dl>                      | Muestra la fecha en formato corto. La cadena de formato predeterminada para este estilo se define mediante la configuración regional \_ SSHORTDATE, que genera una salida como "4/19/96".<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**\_SHORTDATECENTURYFORMAT DTS**</dt> </dl> | **Versión 5,80.** Similar al estilo **\_ SHORTDATEFORMAT de DTS** , excepto que el año es un campo de cuatro dígitos. La cadena de formato predeterminada para este estilo se basa en la configuración regional \_ SSHORTDATE. La salida tiene el siguiente aspecto: "4/19/1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**\_hora DTS**</dt> </dl>                                     | Muestra la hora. La cadena de formato predeterminada para este estilo se define mediante la configuración regional \_ STIMEFORMAT, que produce una salida como "5:31:42 PM".<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**Desactivación de DTS \_**</dt> </dl>                                                 | Coloca un control de flechas a la derecha del control de DTP para modificar los valores de fecha y hora. Este estilo se puede usar en lugar del calendario del mes desplegable, que es el estilo predeterminado.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Observaciones

\_No se pueden combinar los estilos de XXXFORMAT de DTS que definen el formato de presentación. Si ninguno de los estilos de formato es adecuado, use un mensaje [**\_ SETFORMAT de DTM**](dtm-setformat.md) para definir un formato personalizado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





