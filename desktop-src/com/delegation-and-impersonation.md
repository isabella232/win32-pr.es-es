---
title: Delegación y suplantación
description: En escenarios de cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en nombre de un cliente. La situación en la que un servidor tiene la autoridad para actuar en nombre de un cliente se denomina delegación.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369543"
---
# <a name="delegation-and-impersonation"></a>Delegación y suplantación

En escenarios de cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en nombre de un cliente. La situación en la que un servidor tiene la autoridad para actuar en nombre de un cliente se denomina *delegación*.

Desde el punto de vista de la seguridad, surgen dos problemas relacionados con la delegación:

-   ¿Qué debe hacer el servidor al actuar en nombre del cliente?
-   ¿Qué identidad presenta el servidor cuando llama a otros servidores en nombre de un cliente?

Para tratar estos problemas, COM proporciona la siguiente funcionalidad. El cliente puede establecer un *nivel de suplantación* que determine hasta qué punto el servidor podrá actuar como el cliente. Si el cliente concede suficiente autoridad al servidor, el servidor puede suplantar *(simular* ser) al cliente. Al suplantar al cliente, el servidor solo tiene acceso a los objetos o recursos que el cliente tiene permiso para usar. El servidor, que actúa como  cliente, también puede habilitar el enmascaramiento para enmascarar su propia identidad y proyectar la identidad del cliente en llamadas a otros componentes COM.

![Diagrama que muestra cómo el servidor que actúa como el cliente puede habilitar la protección.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Considere el escenario que ilustra la ilustración anterior, donde A y B son procesos en un equipo diferente de C. Procesar A llama a B y B llama a C. El cliente A establece el nivel de suplantación. B establece la funcionalidad de ocultación. Si A establece un nivel de suplantación que permite la suplantación, B puede suplantar a al llamar a C en nombre de A. La identidad que se presenta al proceso C será la identidad de A o la identidad de B, en función de si B habilitó la protección. Si está habilitada la protección, la identidad presentada al proceso C será la de A. Si la protección no está habilitada, la identidad de B se presentará a C.

Para obtener más información, vea los temas siguientes:

-   [Suplantación](impersonation.md)
-   [Niveles de suplantación](impersonation-levels.md)
-   [Ocultación](cloaking.md)

 

 




