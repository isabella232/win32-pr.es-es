---
title: IP Address Control
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de direcciones IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486698"
---
# <a name="ip-address-control"></a>IP Address Control

Esta sección contiene información sobre los elementos de programación utilizados con controles de direcciones IP.

### <a name="overviews"></a>Temas de introducción



| Tema                                          | Contenido                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Controles de direcciones IP](ip-address-controls.md) | Un control de dirección de protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender.<br/> |



 

### <a name="macros"></a>Macros



| Tema                                         | Contenido                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**PRIMERA \_ dirección IP**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | Extrae el valor de campo 0 de una dirección IP empaquetada recuperada con el mensaje de [**\_ GETADDRESS IPM**](ipm-getaddress.md) . <br/> |
| [**CUARTO \_ direcciónIP**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | Extrae el valor del campo 3 de una dirección IP empaquetada recuperada con el mensaje de [**\_ GETADDRESS de IPM**](ipm-getaddress.md) . <br/> |
| [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | Empaqueta cuatro valores de byte en un solo LPARAM adecuado para su uso con el mensaje [**\_ SETADDRESS de IPM**](ipm-setaddress.md) . <br/>  |
| [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | Empaqueta dos valores de byte en un solo LPARAM adecuado para su uso con el mensaje de [**\_ intrange IPM**](ipm-setrange.md) . <br/>       |
| [**SEGUNDA \_ dirección IP**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | Extrae el valor del campo 1 de una dirección IP empaquetada recuperada con el mensaje [**\_ GETADDRESS de IPM**](ipm-getaddress.md) . <br/> |
| [**TERCERA \_ dirección IP**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | Extrae el valor del campo 2 de una dirección IP empaquetada recuperada con el mensaje de [**\_ GETADDRESS de IPM**](ipm-getaddress.md) . <br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                         | Contenido                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**IPM \_ CLEARADDRESS**](ipm-clearaddress.md) | Borra el contenido del control de dirección IP. <br/>                                                                            |
| [**IPM \_ GETADDRESS**](ipm-getaddress.md)     | Obtiene los valores de dirección de los cuatro campos del control de dirección IP. <br/>                                                    |
| [**IPM \_ esblanco**](ipm-isblank.md)           | Determina si todos los campos del control de dirección IP están en blanco. <br/>                                                             |
| [**IPM \_ SETADDRESS**](ipm-setaddress.md)     | Establece los valores de dirección de los cuatro campos en el control de dirección IP. <br/>                                                    |
| [**SETFOCUS de la IPM \_**](ipm-setfocus.md)         | Establece el foco de teclado en el campo especificado en el control de dirección IP. Se seleccionará todo el texto de ese campo. <br/> |
| [**IPM \_ SetRange**](ipm-setrange.md)         | Establece el intervalo válido para el campo especificado en el control de dirección IP. <br/>                                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                     | Contenido                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) | Se envía cuando el usuario cambia un campo en el control o se mueve de un campo a otro. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Estructuras



| Tema                              | Contenido                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | Contiene información del código de notificación [ \_ FIELDCHANGED de IPN](ipn-fieldchanged.md) . <br/> |



 

 

 





