---
description: Dado que los sockets no están representados por el entero de estilo UNIX, pequeño y no negativo, se ha cambiado la implementación de la función SELECT en Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macros Select, FD_SET y FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544862"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Macros Select, FD \_ set y FD \_ XXX

Dado que los sockets no están representados por el entero de estilo UNIX, pequeño y no negativo, se ha cambiado la implementación de la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) en Windows Sockets. Cada conjunto de sockets todavía se representa mediante la estructura del **\_ conjunto FD** , pero en lugar de almacenarse como una máscara de máscara, el conjunto se implementa como una matriz de Sockets. Para evitar posibles problemas, las aplicaciones deben cumplir el uso de las \_ macros FD XXX para establecer, inicializar, borrar y comprobar las estructuras [**de \_ conjuntos FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



