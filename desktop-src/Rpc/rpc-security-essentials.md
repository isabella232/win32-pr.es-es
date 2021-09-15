---
title: RPC Security Essentials
description: Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473579"
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

 

 




