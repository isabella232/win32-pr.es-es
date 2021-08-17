---
title: Autenticación de usuarios
description: El propio protocolo de autenticación puede autenticar al usuario a través de EAP protegido (PEAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3f5d377163f2519d97de847d8d14b5bd96925577a8133988adf8fbf950b283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978375"
---
# <a name="user-authentication"></a>Autenticación de usuarios

El propio protocolo de autenticación puede autenticar al usuario a través de EAP protegido (PEAP). También hay dos proveedores de autenticación integrados en el sistema operativo: Windows autenticación de dominio (a la que se accede a través de servicios de directorio) y servicio de usuario de acceso telefónico remoto (RADIUS).

En el caso de que RADIUS sea el proveedor de autenticación, el complemento EAP se instala en el servidor RADIUS en lugar de en el servidor de punto de acceso inalámbrico (AP), como un servidor RAS. El servidor AP pasa paquetes EAP directamente desde el cliente al servicio de autenticación en el servidor RADIUS. El servidor AP no procesa ninguna de la información de los paquetes EAP, pero debe aceptar las claves de cifrado generadas por PEAP de nivel completo (256 bits) del lado servidor para crear la conexión segura.

 

 




