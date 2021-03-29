---
title: Registro de Server-Side
description: El registro del lado servidor está disponible en un grupo de direcciones URL o una sesión de servidor.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903648"
---
# <a name="server-side-logging"></a>Registro de Server-Side

El registro del lado servidor está disponible en un grupo de direcciones URL o una sesión de servidor. Cuando el registro está habilitado en una sesión de servidor, funciona como una forma centralizada de registro para todos los grupos de direcciones URL en la sesión de servidor. Cuando el registro está habilitado en un grupo de direcciones URL, el registro solo se realiza en las solicitudes que se enrutan al grupo de direcciones URL. La API del servidor HTTP admite los siguientes tipos de registro:

-   [Registro de W3C](w3c-logging.md): disponible en la sesión del servidor y el grupo de direcciones URL.
-   [Registro NCSA](ncsa-logging.md): disponible en el grupo de direcciones URL.
-   [Registro de IIS](iis-logging.md): disponible en el grupo de direcciones URL.
-   [Registro binario centralizado](centralized-binary-logging.md): disponible en la sesión del servidor.

Para aprovechar las ventajas de la característica de registro HTTP, la aplicación habilita y configura un tipo de registro en la sesión de servidor o el grupo de direcciones URL. Para obtener más información, vea [configurar y habilitar el registro del lado servidor](configuring-and-enabling-server-side-logging.md) .

 

 




