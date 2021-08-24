---
title: Controladores de eventos ambiente
description: Controladores de eventos ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Reproductor de Windows Media máscaras, controladores de eventos de ambiente
- máscaras, controladores de eventos de ambiente
- referencia de máscaras, controladores de eventos de ambiente
- controladores de eventos de ambiente
- events,ambient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff72739ec1791b79d6113415f1219a1ddee578b4b5a690ffaaac62bf6b3dbcfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865095"
---
# <a name="ambient-event-handlers"></a>Controladores de eventos ambiente

Los siguientes controladores de eventos se pueden implementar para la mayoría de los elementos de máscara. Los atributos de evento ambiente a los que se accede con la palabra clave **event** se pueden usar dentro de un controlador de eventos para determinar el estado del teclado y el mouse en el momento del evento.



| Controlador de eventos                                   | Descripción                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*atributo* \_ Onchange](attribute-onchange.md) | Cuando un atributo de máscara cambia de valor, se produce un evento que un controlador de eventos puede controlar. El nombre del controlador de eventos es el nombre del atributo seguido de un carácter de subrayado y "onchange", como "value \_ onchange". |
| [onblur](onblur.md)                            | Controla un evento que tiene lugar cuando el elemento pierde el foco del teclado.                                                                                                                                                       |
| [Onclick](onclick.md)                          | Controla un evento que tiene lugar cuando el usuario hace clic en el elemento.                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | Controla un evento que tiene lugar cuando el usuario hace doble clic en el elemento.                                                                                                                                                         |
| [onephablend](onendalphablend.md)          | Controla un evento que tiene lugar cuando un elemento completa una **operación alphaBlendTo.**                                                                                                                                         |
| [onendmove](onendmove.md)                      | Controla un evento que tiene lugar cuando un elemento completa una **operación moveTo.**                                                                                                                                                |
| [onfocus](onfocus.md)                          | Controla un evento que tiene lugar cuando el elemento recibe el foco del teclado.                                                                                                                                                    |
| [onkeydown](onkeydown.md)                      | Controla un evento que tiene lugar cuando se presiona una tecla.                                                                                                                                                                           |
| [Onkeypress](onkeypress.md)                    | Controla un evento que tiene lugar cuando el usuario presiona una tecla alfanumérica.                                                                                                                                                       |
| [onkeyup](onkeyup.md)                          | Controla un evento que tiene lugar cuando se libera una clave.                                                                                                                                                                          |
| [onmousedown](onmousedown.md)                  | Controla un evento que tiene lugar cuando el usuario hace clic en un botón del mouse.                                                                                                                                                             |
| [Onmousemove](onmousemove.md)                  | Controla un evento que tiene lugar cuando el usuario mueve el puntero del mouse mientras está sobre un elemento.                                                                                                                               |
| [onmouseout](onmouseout.md)                    | Controla un evento que tiene lugar cuando el usuario mueve el puntero fuera del elemento.                                                                                                                                                 |
| [Onmouseover](onmouseover.md)                  | Controla un evento que tiene lugar cuando el usuario coloca por primera vez el puntero sobre el elemento.                                                                                                                                         |
| [onmouseup](onmouseup.md)                      | Controla un evento que tiene lugar cuando el usuario suelta un botón del mouse mientras el puntero está sobre el elemento.                                                                                                                     |
| [Onresize](onresize.md)                        | Controla un evento que tiene lugar cuando cambia el tamaño de un control.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de evento ambiente**](ambient-event-attributes.md)
</dt> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




