---
description: Una aplicación de servidor proporciona servicios a los clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Cliente o servidor Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160847"
---
# <a name="clientserver-access-control"></a>Cliente o servidor Access Control

Una aplicación de servidor proporciona servicios a los clientes. Por ejemplo, un servidor podría realizar los siguientes servicios en nombre de un cliente:

-   Guardar y recuperar información de una base de datos privada
-   Acceso a recursos de red
-   Iniciar [*procesos*](/windows/desktop/SecGloss/p-gly) en el contexto de [*seguridad del cliente*](/windows/desktop/SecGloss/s-gly) en el equipo del servidor

Un servidor protegido controla el acceso a sus servicios. Windows proporciona compatibilidad de seguridad que permite a un servidor hacer lo siguiente:

-   Suplantar el contexto de seguridad de un [*cliente,*](/windows/desktop/SecGloss/s-gly) [](/windows/desktop/SecGloss/p-gly) lo que hace que el sistema realice la mayoría de las comprobaciones de acceso y privilegios en el [*token*](/windows/desktop/SecGloss/a-gly) de acceso del cliente en lugar del del servidor.
-   Iniciar sesión de un cliente en el equipo del servidor
-   Conectar a recursos de red mediante el contexto de seguridad del cliente
-   Creación [*de descriptores de seguridad*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados
-   Determinar si un descriptor de seguridad permite el acceso a un cliente
-   Determinar si un conjunto de privilegios está habilitado en el token de un cliente
-   Generar mensajes de auditoría en el registro de eventos de seguridad para registrar los intentos de un cliente de acceder a objetos o usar privilegios

 

 
