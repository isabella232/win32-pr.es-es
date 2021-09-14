---
description: Puesto que los sockets no se representan mediante el entero de estilo UNIX, pequeño y no negativo, la implementación de la función select se cambió en Windows sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Seleccionar, FD_SET y FD_XXX macros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063967"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Macros Select, FD \_ SET y FD \_ XXX

Puesto que los sockets no se representan mediante el entero de estilo UNIX, pequeño y no negativo, la implementación de la función [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) se cambió en Windows Sockets. Cada conjunto de sockets sigue representado por la estructura **FD \_ SET,** pero en lugar de almacenarse como máscara de bits, el conjunto se implementa como una matriz de sockets. Para evitar posibles problemas, las aplicaciones deben cumplir el uso de las macros XXX de FD para establecer, inicializar, borrar y \_ comprobar las estructuras de FD [**\_ SET.**](/windows/desktop/api/winsock/nf-winsock-fd_set)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



