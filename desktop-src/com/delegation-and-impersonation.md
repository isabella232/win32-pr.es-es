---
title: Delegación y suplantación
description: En escenarios cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en el nombre de un cliente. La situación en la que se proporciona a un servidor la autoridad para actuar en nombre de un cliente se denomina delegación.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553612"
---
# <a name="delegation-and-impersonation"></a>Delegación y suplantación

En escenarios cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en el nombre de un cliente. La situación en la que se proporciona a un servidor la autoridad para actuar en nombre de un cliente se denomina *delegación*.

Desde el punto de vista de la seguridad, surgen dos problemas relacionados con la delegación:

-   ¿Qué debe permitir el servidor cuando actúa en nombre del cliente?
-   ¿Qué identidad presenta el servidor cuando llama a otros servidores en nombre de un cliente?

Para solucionar estos problemas, COM proporciona la siguiente funcionalidad. El cliente puede establecer un *nivel de suplantación* que determina en qué medida el servidor podrá actuar como el cliente. Si el cliente concede suficiente autoridad para el servidor, el servidor puede *Suplantar* (fingir ser) el cliente. Al suplantar al cliente, al servidor se le concede acceso solo a los objetos o recursos que el cliente tiene permiso para usar. El servidor, que actúa como cliente, también puede habilitar la *ocultación* para enmascarar su propia identidad y proyectar la identidad del cliente en llamadas a otros componentes com.

![Diagrama que muestra cómo el servidor que actúa como cliente puede habilitar la ocultación.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Considere el escenario que se muestra en la ilustración anterior, donde A y B son procesos en un equipo diferente de C. procesar una llamada B y B llama a C. el cliente A establece el nivel de suplantación. B establece la funcionalidad de ocultación. Si un establece un nivel de suplantación que permite la suplantación, B puede suplantar A cuando se llama a C en nombre de. La identidad que se presenta al proceso C será la identidad o la identidad de B, en función de si la ocultación fue habilitada por B. Si está habilitada la ocultación, la identidad presentada al proceso C será la de. Si el Cloaking no está habilitado, la identidad de B se presentará en C.

Para obtener más información, vea los temas siguientes:

-   [Suplantación](impersonation.md)
-   [Niveles de suplantación](impersonation-levels.md)
-   [Esconder](cloaking.md)

 

 




