---
title: Server-Side registro
description: El registro del lado servidor está disponible en un grupo de direcciones URL o en una sesión de servidor.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8caf7475fe6d2b408f6e2a1f924bad73df64c315ef5e0acd1c7c317ce5eac6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829845"
---
# <a name="server-side-logging"></a>Server-Side registro

El registro del lado servidor está disponible en un grupo de direcciones URL o en una sesión de servidor. Cuando el registro está habilitado en una sesión de servidor, funciona como forma centralizada de registro para todos los grupos de direcciones URL en la sesión del servidor. Cuando el registro está habilitado en un grupo de direcciones URL, el registro solo se realiza en las solicitudes que se enruta al grupo de direcciones URL. La API de servidor HTTP admite los siguientes tipos de registro:

-   [Registro de W3C:](w3c-logging.md)disponible en la sesión del servidor y en el grupo de direcciones URL.
-   [Registro de NCSA:](ncsa-logging.md)disponible en el grupo de direcciones URL.
-   [Registro de IIS:](iis-logging.md)disponible en el grupo de direcciones URL.
-   [Registro binario centralizado:](centralized-binary-logging.md)disponible en la sesión del servidor.

Para aprovechar las ventajas de la característica de registro HTTP, la aplicación habilita y configura un tipo de registro en la sesión del servidor o el grupo de direcciones URL. Para obtener más información, vea [Configuring and Enabling Server Side Logging (Configuración y habilitación del registro del lado servidor).](configuring-and-enabling-server-side-logging.md)

 

 




