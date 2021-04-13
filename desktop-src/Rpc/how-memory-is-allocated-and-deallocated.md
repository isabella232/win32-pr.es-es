---
title: Asignación y desasignación de memoria
description: De forma predeterminada, el código auxiliar generado por el compilador MIDL llama a las funciones proporcionadas por el usuario para asignar y liberar memoria. Estas funciones, denominadas \_ asignación de usuarios \_ de MIDL y usuarios de MIDL \_ \_ , deben ser proporcionadas por el desarrollador y vinculadas a la aplicación.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c32ac4d33fbd67f617f79125921ddfffc0de5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421113"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Asignación y desasignación de memoria

De forma predeterminada, el código auxiliar generado por el compilador MIDL llama a las funciones proporcionadas por el usuario para asignar y liberar memoria. Estas funciones, denominadas [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) y [**usuarios de MIDL \_ \_**](/windows/desktop/Midl/midl-user-free-1), deben ser proporcionadas por el desarrollador y vinculadas a la aplicación.

Todas las aplicaciones deben proporcionar implementaciones de la [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) y el usuario de [**MIDL \_ \_ gratis**](/windows/desktop/Midl/midl-user-free-1), aunque es posible que los nombres de estas funciones no aparezcan explícitamente en el código auxiliar. La única excepción es cuando se compila en modo de compatibilidad de OSF (/OSF). Estas funciones proporcionadas por el usuario deben coincidir con un prototipo de función definido específico, pero de lo contrario, se pueden implementar de cualquier manera que sea conveniente o útil para la aplicación. Como alternativa, las aplicaciones pueden usar el paquete de administración de memoria RpcSs. La biblioteca en tiempo de ejecución de Microsoft RPC proporciona este grupo de funciones.

En las secciones siguientes se describen las funciones de administración de memoria RPC.

-   [**\_asignación de usuarios de MIDL \_**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**usuario de MIDL \_ \_ gratis**](/windows/desktop/Midl/midl-user-free-1)
-   [Paquete de administración de memoria RpcSs](rpcss-memory-management-package.md)

 

 