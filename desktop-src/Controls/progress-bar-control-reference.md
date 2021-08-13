---
title: ProgressBar
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de barra de progreso.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c9cd66326336cd3733f881f3f19d82fedc3bf8d8420f83035bf20dc914c7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670656"
---
# <a name="progress-bar"></a>ProgressBar

Esta sección contiene información sobre los elementos de programación utilizados con controles de barra de progreso.

### <a name="overviews"></a>Temas de introducción



| Tema                                            | Contenido                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Control barra de progreso](progress-bar-control.md) | Una barra de progreso es una ventana que una aplicación puede usar para indicar el progreso de una operación larga.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                       | Contenido                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBM \_ DELTAPOS**](pbm-deltapos.md)       | Avanza la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición. <br/>                                                                                                                                 |
| [**PBM \_ GETBARCOLOR**](pbm-getbarcolor.md) | Obtiene el color de la barra de progreso.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETBKCOLOR**](pbm-getbkcolor.md)   | Obtiene el color de fondo de la barra de progreso.<br/>                                                                                                                                                                                                             |
| [**PBM \_ GETPOS**](pbm-getpos.md)           | Recupera la posición actual de la barra de progreso. <br/>                                                                                                                                                                                                       |
| [**PBM \_ GETRANGE**](pbm-getrange.md)       | Recupera información sobre los límites altos y bajos actuales de un control de barra de progreso determinado. <br/>                                                                                                                                                              |
| [**PBM \_ GETSTATE**](pbm-getstate.md)       | Obtiene el estado de la barra de progreso.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETSTEP**](pbm-getstep.md)         | Recupera el incremento de paso para una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un [**mensaje \_ STEPIT de PBM.**](pbm-stepit.md)<br/>                                               |
| [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) | Establece el color de la barra de indicadores de progreso en el control de barra de progreso. <br/>                                                                                                                                                                                 |
| [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md)   | Establece el color de fondo en la barra de progreso. <br/>                                                                                                                                                                                                            |
| [**PBM \_ SETMARQUEE**](pbm-setmarquee.md)   | Establece la barra de progreso en modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.<br/>                                                                                                                                                                |
| [**PBM \_ SETPOS**](pbm-setpos.md)           | Establece la posición actual de una barra de progreso y vuelve a dibujar la barra para reflejar la nueva posición. <br/>                                                                                                                                                             |
| [**PBM \_ SETRANGE**](pbm-setrange.md)       | Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.<br/>                                                                                                                                                       |
| [**PBM \_ SETRANGE32**](pbm-setrange32.md)   | Establece el intervalo de un control de barra de progreso en un valor de 32 bits. <br/>                                                                                                                                                                                               |
| [**PBM \_ SETSTATE**](pbm-setstate.md)       | Establece el estado de la barra de progreso.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ SETSTEP**](pbm-setstep.md)         | Especifica el incremento de paso para una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un [**mensaje \_ STEPIT de PBM.**](pbm-stepit.md) De forma predeterminada, el incremento de paso se establece en 10. <br/> |
| [**PBM \_ STEPIT**](pbm-stepit.md)           | Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento de paso mediante el envío del [**mensaje \_ SETSTEP de PBM.**](pbm-setstep.md) <br/>                                |



 

### <a name="structures"></a>Estructuras



| Tema                      | Contenido                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Contiene información sobre los límites altos y bajos de un control de barra de progreso. Esta estructura se usa con el [**mensaje \_ GETRANGE de PBM.**](pbm-getrange.md) <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                                          | Contenido                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Estilos de control de barra de progreso](progress-bar-control-styles.md) | Los siguientes estilos de control son compatibles con los **controles de barra de** progreso:<br/> |



 

 

 





