---
description: El cajero automático se encuentra en la categoría de datos raíz y planos de control con raíz.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Punto de cajero automático a multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198d8160fdb1e942cc581374af18ca57303726bdddd41142855d366e58dfbf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504465"
---
# <a name="atm-point-to-multipoint"></a>Punto de cajero automático a multipunto

El cajero automático se encuentra en la categoría de datos raíz y planos de control con raíz. Una aplicación que actúa como raíz crearía sockets raíz de c y los homólogos que se ejecutan en nodos \_ hoja utilizarían \_ sockets hoja de c. La aplicación raíz usa [**WSAJoinLeaf para**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) agregar nuevos nodos hoja. Las aplicaciones correspondientes en los nodos hoja habrán establecido sus sockets hoja c \_ en modo de escucha. **WSAJoinLeaf con** un socket raíz c especificado se asigna al mensaje \_ ADDPARTY de Q.2931. La combinación iniciada por hoja no se admite en ATM UNI 3.1, pero se admite en ATM UNI 4.0. Por **lo tanto, WSAJoinLeaf** con un socket hoja c especificado se asigna al \_ mensaje UNI 4.0 de ATM adecuado.

Hay consideraciones adicionales que se deben tener en cuenta para el punto a varios puntos de ATM:

-   La adición de nuevas hojas a la sesión de punto a multipunto de ATM solo se basa en la invitación. La raíz invita a las hojas , que ya tienen su llamada de función [**accept,**](/windows/desktop/api/Winsock2/nf-winsock2-accept) mediante una llamada a la [**función WSAJoinLeaf.**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)
-   El flujo de datos de una sesión de punto a multipunto de ATM es solo de raíz a hoja. leaves no puede usar la misma sesión para enviar información a la raíz.
-   Solo se permite una hoja por adaptador de ATM.

 

 



