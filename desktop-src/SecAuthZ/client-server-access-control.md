---
description: Una aplicación de servidor proporciona servicios a los clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Cliente/servidor Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c943d9d1e1f1cc5dcc405f49ab200aa30618f7eefb86c7f26342f005f23249fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782730"
---
# <a name="clientserver-access-control"></a>Cliente/servidor Access Control

Una aplicación de servidor proporciona servicios a los clientes. Por ejemplo, un servidor podría realizar los siguientes servicios en nombre de un cliente:

-   Guardar y recuperar información de una base de datos privada
-   Acceso a recursos de red
-   Iniciar [*procesos*](/windows/desktop/SecGloss/p-gly) en el contexto de seguridad [*del cliente*](/windows/desktop/SecGloss/s-gly) en el equipo del servidor

Un servidor protegido controla el acceso a sus servicios. Windows proporciona compatibilidad de seguridad que permite a un servidor hacer lo siguiente:

-   Suplantar el contexto de seguridad de un [*cliente,*](/windows/desktop/SecGloss/s-gly) [](/windows/desktop/SecGloss/p-gly) lo que hace que el sistema realice la mayoría de las comprobaciones de acceso y privilegios en el [*token*](/windows/desktop/SecGloss/a-gly) de acceso del cliente en lugar del del servidor.
-   Inicio de sesión de un cliente en el equipo del servidor
-   Conectar a recursos de red mediante el contexto de seguridad del cliente
-   Creación [*de descriptores de seguridad*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados
-   Determinar si un descriptor de seguridad permite el acceso a un cliente
-   Determinar si un conjunto de privilegios está habilitado en el token de un cliente
-   Generación de mensajes de auditoría en el registro de eventos de seguridad para registrar los intentos de un cliente de acceder a objetos o usar privilegios

 

 
