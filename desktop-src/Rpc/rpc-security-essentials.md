---
title: RPC Security Essentials
description: Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed8bce6f97ecfc7bd257d20eebbb35d068624fe017c01a662b47fceb463b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926036"
---
# <a name="rpc-security-essentials"></a>RPC Security Essentials

Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor. Para obtener más información sobre los enlaces, vea [Binding and Handles](binding-and-handles.md). Para completar una llamada de procedimiento remoto seguro, son necesarios pasos adicionales. En primer lugar, el servidor debe elegir un proveedor de seguridad (servicio de autenticación en terminología de DCE). A continuación, debe decidir sobre su mecanismo de autenticación. Después de eso, el cliente obtiene un enlace al servidor y solicita una llamada a procedimiento remoto seguro desde el tiempo de ejecución rpc y especifica varias opciones de seguridad, como el proveedor de seguridad, las opciones de QOS de seguridad, y así sucesivamente.

En esta sección se explican los conceptos esenciales y la información necesaria para usar las funciones RPC para crear un cliente y un servidor para una aplicación distribuida autenticada. Se organiza en los temas siguientes:

-   [Nombres principales](principal-names.md)
-   [Niveles de autenticación](authentication-levels.md)
-   [Servicios de autenticación](authentication-services.md)
-   [Credenciales de autenticación de cliente](client-authentication-credentials.md)
-   [Servicios de autorización](authorization-services.md)
-   [Calidad de servicio](quality-of-service.md)
-   [Funciones de autorización](authorization-functions.md)
-   [Funciones de adquisición de claves](key-acquisition-functions.md)
-   [Suplantación de cliente](client-impersonation.md)

 

 




