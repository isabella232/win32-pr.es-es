---
description: ATM entra en la categoría de los datos raíz y los planos de control raíz.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Punto de ATM a multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715145"
---
# <a name="atm-point-to-multipoint"></a>Punto de ATM a multipoint

ATM entra en la categoría de los datos raíz y los planos de control raíz. Una aplicación que actúa como raíz crearía \_ Sockets raíz de c y los homólogos que se ejecutan en los nodos hoja usarían \_ sockets de hojas de c. La aplicación raíz usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar nuevos nodos hoja. Las aplicaciones correspondientes en los nodos de hoja habrán establecido sus \_ sockets de hoja de c en modo de escucha. **WSAJoinLeaf** con un \_ socket raíz de c especificado se asigna al mensaje Q. 2931 ADDPARTY. La combinación iniciada por hoja no se admite en el UNI 3,1 de ATM, pero se admite en la plataforma ATM UNI 4,0. Por lo tanto, **WSAJoinLeaf** con un socket de hoja de c \_ especificado se asigna al mensaje unidireccional 4,0 de ATM adecuado.

Existen consideraciones adicionales que se deben tener en cuenta para los puntos de Multipoint ATM:

-   La adición de nuevas hojas a la sesión de punto a multipunto de ATM solo se basa en la invitación. Los invitados raíz salen (que ya tienen la llamada de función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ) mediante una llamada a la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   El flujo de datos en una sesión de punto a multipunto de ATM es solo de raíz a lugar de salida; las hojas no pueden usar la misma sesión para enviar información a la raíz.
-   Solo se permite una hoja por cada adaptador ATM.

 

 



