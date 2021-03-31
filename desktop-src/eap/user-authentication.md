---
title: Autenticación de usuarios
description: El propio protocolo de autenticación puede autenticar al usuario a través de EAP protegido (PEAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785105"
---
# <a name="user-authentication"></a>Autenticación de usuarios

El propio protocolo de autenticación puede autenticar al usuario a través de EAP protegido (PEAP). También hay dos proveedores de autenticación integrados en el sistema operativo: autenticación de dominio de Windows (a la que se tiene acceso a través de los servicios de directorio) y servicio de autenticación remota telefónica de usuario (RADIUS).

En el caso de que RADIUS sea el proveedor de autenticación, el complemento EAP se instala en el servidor RADIUS en lugar de en el servidor de punto de acceso inalámbrico (AP), como un servidor RAS. El servidor de AP pasa los paquetes EAP directamente desde el cliente al servicio de autenticación en el servidor RADIUS. El servidor de AP no procesa ninguna información de los paquetes EAP, pero debe aceptar las claves de cifrado generadas por PEAP de nivel de servidor y de seguridad completa (256 bits) para crear la conexión segura.

 

 




