---
title: Trabajar con un servidor de estado
description: NPS realiza la autenticación mediante una base de datos que está configurada en el sitio del servidor NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685736"
---
# <a name="working-with-a-state-server"></a>Trabajar con un servidor de estado

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

NPS realiza la autenticación mediante una base de datos que está configurada en el sitio del servidor NPS. Esta base de datos de autenticación podría ser la base de datos de usuario de un dominio de Windows o podría dibujarse en la información de usuario obtenida del Active Directory de Windows. En el diagrama siguiente se muestra una configuración típica que muestra cómo interactúa NPS con las bases de datos de autenticación, como una base de datos de usuario de dominio de Windows o Active Directory. En el diagrama también se muestra cómo NPS puede interactuar con un servidor de estado proporcionado por terceros. El propósito principal de un servidor de estado es limitar el número de sesiones de inicio de sesión simultáneas que puede ejecutar un solo usuario.

![interacción de NPS con el servidor de estado y las bases de datos de autenticación](images/ias02.png)

Hay dos puntos de interacción entre NPS y el servidor de estado. Una interacción tiene lugar cuando NPS recibe una solicitud de autenticación del NAS. El servidor de estado proporciona información de su base de datos para determinar si se debe aceptar o denegar la solicitud. La otra interacción tiene lugar cuando NPS recibe solicitudes de cuentas del NAS. El servidor de estado usa la información de estas solicitudes de cuentas para actualizar su base de datos.

Para obtener más información sobre los servidores de estado, vea:

-   [Consideraciones sobre el diseño del servidor de estado](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de autenticación de Internet y servidor de directivas de redes](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticación, autorización y cuentas RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registro con servidor de directivas de redes](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 