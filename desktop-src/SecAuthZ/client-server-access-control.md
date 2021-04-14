---
description: Una aplicación de servidor proporciona servicios a los clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Access Control cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648235"
---
# <a name="clientserver-access-control"></a>Access Control cliente/servidor

Una aplicación de servidor proporciona servicios a los clientes. Por ejemplo, un servidor podría realizar los siguientes servicios en nombre de un cliente:

-   Guardar y recuperar información de una base de datos privada
-   Acceder a los recursos de red
-   Iniciar [*procesos*](/windows/desktop/SecGloss/p-gly) en el contexto de [*seguridad*](/windows/desktop/SecGloss/s-gly) del cliente en el equipo del servidor

Un servidor protegido controla el acceso a sus servicios. Windows proporciona compatibilidad de seguridad que permite que un servidor haga lo siguiente:

-   Suplantar el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly)de un cliente, que hace que el sistema realice la mayoría de las comprobaciones de [*privilegios*](/windows/desktop/SecGloss/p-gly) y de acceso en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del cliente en lugar de en el servidor
-   Iniciar una sesión de cliente en el equipo del servidor
-   Conectarse a recursos de red mediante el contexto de seguridad del cliente
-   Crear [*descriptores de seguridad*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados
-   Determinar si un descriptor de seguridad permite el acceso a un cliente
-   Determinar si un conjunto de privilegios está habilitado en el token de un cliente
-   Generar mensajes de auditoría en el registro de eventos de seguridad para registrar intentos de un cliente para obtener acceso a objetos o usar privilegios

 

 
