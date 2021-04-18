---
title: ProgressBar
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de progreso.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b99a31bbbd3b80de0d528d5232c79c28af1e1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656271"
---
# <a name="progress-bar"></a>ProgressBar

Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de progreso.

### <a name="overviews"></a>Temas de introducción



| Tema                                            | Contenido                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Control de barra de progreso](progress-bar-control.md) | Una barra de progreso es una ventana que una aplicación puede utilizar para indicar el progreso de una operación larga.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                       | Contenido                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELTAPOS de PBM \_**](pbm-deltapos.md)       | Hace avanzar la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición. <br/>                                                                                                                                 |
| [**GETBARCOLOR de PBM \_**](pbm-getbarcolor.md) | Obtiene el color de la barra de progreso.<br/>                                                                                                                                                                                                                        |
| [**GETBKCOLOR de PBM \_**](pbm-getbkcolor.md)   | Obtiene el color de fondo de la barra de progreso.<br/>                                                                                                                                                                                                             |
| [**GETPOS de PBM \_**](pbm-getpos.md)           | Recupera la posición actual de la barra de progreso. <br/>                                                                                                                                                                                                       |
| [**GETRANGE de PBM \_**](pbm-getrange.md)       | Recupera información sobre los límites máximo y mínimo actuales de un control de barra de progreso determinado. <br/>                                                                                                                                                              |
| [**GETSTATE de PBM \_**](pbm-getstate.md)       | Obtiene el estado de la barra de progreso.<br/>                                                                                                                                                                                                                        |
| [**GETSTEP de PBM \_**](pbm-getstep.md)         | Recupera el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de [**\_ STEPIT de PBM**](pbm-stepit.md) .<br/>                                               |
| [**SETBARCOLOR de PBM \_**](pbm-setbarcolor.md) | Establece el color de la barra de indicador de progreso en el control de barra de progreso. <br/>                                                                                                                                                                                 |
| [**SETBKCOLOR de PBM \_**](pbm-setbkcolor.md)   | Establece el color de fondo de la barra de progreso. <br/>                                                                                                                                                                                                            |
| [**SETMARQUEE de PBM \_**](pbm-setmarquee.md)   | Establece la barra de progreso en el modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.<br/>                                                                                                                                                                |
| [**SETPOS de PBM \_**](pbm-setpos.md)           | Establece la posición actual de una barra de progreso y vuelve a dibujar la barra para reflejar la nueva posición. <br/>                                                                                                                                                             |
| [**SetRange de PBM \_**](pbm-setrange.md)       | Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.<br/>                                                                                                                                                       |
| [**SETRANGE32 de PBM \_**](pbm-setrange32.md)   | Establece el intervalo de un control de barra de progreso en un valor de 32 bits. <br/>                                                                                                                                                                                               |
| [**PBM \_ SETSTATE**](pbm-setstate.md)       | Establece el estado de la barra de progreso.<br/>                                                                                                                                                                                                                        |
| [**SETSTEP de PBM \_**](pbm-setstep.md)         | Especifica el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de [**\_ STEPIT de PBM**](pbm-stepit.md) . De forma predeterminada, el incremento de paso se establece en 10. <br/> |
| [**STEPIT de PBM \_**](pbm-stepit.md)           | Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento del paso mediante el envío del mensaje de [**\_ SETSTEP de PBM**](pbm-setstep.md) . <br/>                                |



 

### <a name="structures"></a>Estructuras



| Tema                      | Contenido                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Contiene información sobre los límites superior e inferior de un control de barra de progreso. Esta estructura se usa con el mensaje de [**\_ GETRANGE de PBM**](pbm-getrange.md) . <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                                          | Contenido                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Estilos de control de barra de progreso](progress-bar-control-styles.md) | Los controles de **barra de progreso** admiten los siguientes estilos de control:<br/> |



 

 

 





