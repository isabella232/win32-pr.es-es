---
title: Delegación y suplantación
description: En escenarios de cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en nombre de un cliente. La situación en la que un servidor tiene la autoridad para actuar en nombre de un cliente se denomina delegación.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00f878c7bc0a37e7d60c246550ff404ed4d0c31312610ab63d1863b34aa52be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919485"
---
# <a name="delegation-and-impersonation"></a>Delegación y suplantación

En escenarios de cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en nombre de un cliente. La situación en la que un servidor tiene la autoridad para actuar en nombre de un cliente se denomina *delegación*.

Desde el punto de vista de la seguridad, surgen dos problemas relacionados con la delegación:

-   ¿Qué debe hacer el servidor al actuar en nombre del cliente?
-   ¿Qué identidad presenta el servidor cuando llama a otros servidores en nombre de un cliente?

Para tratar estos problemas, COM proporciona la siguiente funcionalidad. El cliente puede establecer un *nivel de suplantación* que determine en qué medida el servidor podrá actuar como cliente. Si el cliente concede suficiente autoridad al servidor, el servidor puede *suplantar* (simular ser) al cliente. Al suplantar al cliente, el servidor solo tiene acceso a los objetos o recursos que el cliente tiene permiso para usar. El servidor, que actúa como  cliente, también puede habilitar la activación para enmascarar su propia identidad y proyectar la identidad del cliente en llamadas a otros componentes COM.

![Diagrama en el que se muestra cómo el servidor que actúa como cliente puede habilitar la activación.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Considere el escenario que se muestra en la ilustración anterior, donde A y B son procesos en un equipo diferente de C. El proceso A llama a B y B llama a C. El cliente A establece el nivel de suplantación. B establece la funcionalidad de ocultación. Si A establece un nivel de suplantación que permite la suplantación, B puede suplantar A al llamar a C en nombre de A. La identidad que se presenta para procesar C será la identidad de A o la identidad de B, dependiendo de si B ha habilitado la protección. Si está habilitada la protección, la identidad presentada al proceso C será la de A. Si la protección no está habilitada, la identidad de B se presentará a C.

Para obtener más información, vea los temas siguientes:

-   [Suplantación](impersonation.md)
-   [Niveles de suplantación](impersonation-levels.md)
-   [Ocultación](cloaking.md)

 

 




