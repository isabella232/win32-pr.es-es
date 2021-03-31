---
title: Controladores de eventos de ambiente
description: Controladores de eventos de ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Aspectos de Windows Media Player, controladores de eventos de ambiente
- máscaras, controladores de eventos de ambiente
- referencia para máscaras, controladores de eventos de ambiente
- Controladores de eventos de ambiente
- eventos, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418479"
---
# <a name="ambient-event-handlers"></a>Controladores de eventos de ambiente

Los controladores de eventos siguientes se pueden implementar para la mayoría de los elementos de máscara. Los atributos de evento de ambiente a los que se tiene acceso con la palabra clave **Event** se pueden usar dentro de un controlador de eventos para determinar el estado del teclado y del mouse en el momento del evento.



| Controlador de eventos                                   | Descripción                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*atributo* \_ de onchange](attribute-onchange.md) | Cuando un atributo de máscara cambia de valor, se produce un evento que se puede controlar mediante un controlador de eventos. El nombre del controlador de eventos es el nombre del atributo seguido por un carácter de subrayado y "onchange", como "valor onchange \_ ". |
| [onblur](onblur.md)                            | Controla un evento que se produce cuando el elemento pierde el foco de teclado.                                                                                                                                                       |
| [AlHacerClic](onclick.md)                          | Controla un evento que se produce cuando el usuario hace clic en el elemento.                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | Controla un evento que se produce cuando el usuario hace doble clic en el elemento.                                                                                                                                                         |
| [onendalphablend](onendalphablend.md)          | Controla un evento que se produce cuando un elemento completa una operación **alphaBlendTo** .                                                                                                                                         |
| [onendmove](onendmove.md)                      | Controla un evento que se produce cuando un elemento completa una operación **moveTo** .                                                                                                                                                |
| [onfocus](onfocus.md)                          | Controla un evento que se produce cuando el elemento recibe el foco de teclado.                                                                                                                                                    |
| [onkeydown](onkeydown.md)                      | Controla un evento que se produce cuando se presiona una tecla.                                                                                                                                                                           |
| [onkeypress](onkeypress.md)                    | Controla un evento que se produce cuando el usuario presiona una clave alfanumérica.                                                                                                                                                       |
| [AlSubirTecla](onkeyup.md)                          | Controla un evento que se produce cuando se suelta una tecla.                                                                                                                                                                          |
| [alsubirmouse](onmousedown.md)                  | Controla un evento que se produce cuando el usuario hace clic en un botón del mouse.                                                                                                                                                             |
| [almovermouse](onmousemove.md)                  | Controla un evento que se produce cuando el usuario mueve el puntero del mouse mientras se encuentra sobre un elemento.                                                                                                                               |
| [onmouseout](onmouseout.md)                    | Controla un evento que se produce cuando el usuario mueve el puntero fuera del elemento.                                                                                                                                                 |
| [onmouseover](onmouseover.md)                  | Controla un evento que se produce cuando el usuario coloca por primera vez el puntero sobre el elemento.                                                                                                                                         |
| [OnMouseUp](onmouseup.md)                      | Controla un evento que se produce cuando el usuario suelta un botón del mouse mientras el puntero está sobre el elemento.                                                                                                                     |
| [OnResize](onresize.md)                        | Controla un evento que se produce cuando se cambia el tamaño de un control.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de evento de ambiente**](ambient-event-attributes.md)
</dt> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




