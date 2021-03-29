---
title: Aspectos básicos de seguridad de RPC
description: Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903785"
---
# <a name="rpc-security-essentials"></a>Aspectos básicos de seguridad de RPC

Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor. Para obtener más información sobre los enlaces, vea [enlazar y controlar](binding-and-handles.md). Para completar una llamada de procedimiento remoto segura, se necesitan pasos adicionales. En primer lugar, el servidor debe elegir un proveedor de seguridad (servicio de autenticación en la terminología de DCE). Después, debe decidirse por su mecanismo de autenticación. Después, el cliente obtiene un enlace al servidor y solicita una llamada de procedimiento remoto segura desde el tiempo de ejecución de RPC, y especifica diversas opciones de seguridad, como el proveedor de seguridad, las opciones de QOS de seguridad, etc.

En esta sección se explican los conceptos y la información esenciales necesarios para utilizar las funciones de RPC con el fin de crear un cliente y un servidor para una aplicación distribuida autenticada. Se organiza en los temas siguientes:

-   [Nombres principales](principal-names.md)
-   [Niveles de autenticación](authentication-levels.md)
-   [Servicios de autenticación](authentication-services.md)
-   [Credenciales de autenticación del cliente](client-authentication-credentials.md)
-   [Servicios de autorización](authorization-services.md)
-   [Calidad de servicio](quality-of-service.md)
-   [Funciones de autorización](authorization-functions.md)
-   [Funciones de adquisición de claves](key-acquisition-functions.md)
-   [Suplantación de cliente](client-impersonation.md)

 

 




