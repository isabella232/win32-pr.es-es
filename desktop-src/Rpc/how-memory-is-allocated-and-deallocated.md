---
title: Cómo se asigna y desasigna la memoria
description: De forma predeterminada, el código auxiliar generado por el compilador MIDL llama a las funciones proporcionadas por el usuario para asignar y liberar memoria. Estas funciones, denominadas midl user allocate y midl user free, deben ser proporcionadas por el desarrollador \_ \_ y \_ \_ vinculadas a la aplicación.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c32ac4d33fbd67f617f79125921ddfffc0de5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244689"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Cómo se asigna y desasigna la memoria

De forma predeterminada, el código auxiliar generado por el compilador MIDL llama a las funciones proporcionadas por el usuario para asignar y liberar memoria. Estas funciones, [**denominadas midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) y [**midl user \_ \_ free,**](/windows/desktop/Midl/midl-user-free-1)deben ser proporcionadas por el desarrollador y vinculadas a la aplicación.

Todas las aplicaciones deben proporcionar implementaciones de [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) y [**midl \_ user \_ free,**](/windows/desktop/Midl/midl-user-free-1)aunque es posible que los nombres de estas funciones no aparezcan explícitamente en los códigos auxiliares. La única excepción es cuando se compila en modo de compatibilidad con OSF (/osf). Estas funciones proporcionadas por el usuario deben coincidir con un prototipo de función definido específico, pero de lo contrario, se pueden implementar de cualquier manera que sea conveniente o útil para la aplicación. Como alternativa, las aplicaciones pueden usar el paquete de administración de memoria rpcSs. La biblioteca en tiempo de ejecución rpc de Microsoft proporciona este grupo de funciones.

En las secciones siguientes se describen las funciones de administración de memoria rpc.

-   [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1)
-   [Paquete de administración de memoria rpcSs](rpcss-memory-management-package.md)

 

 