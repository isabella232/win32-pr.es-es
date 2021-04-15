---
description: El usuario puede iniciar un servicio con la utilidad servicios del panel de control. El usuario puede especificar argumentos para el servicio en el campo parámetros de inicio. Un programa de control de servicios puede iniciar un servicio y especificar sus argumentos con la función StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Inicio de servicios a petición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668455"
---
# <a name="starting-services-on-demand"></a>Inicio de servicios a petición

El usuario puede iniciar un servicio con la utilidad servicios del panel de control. El usuario puede especificar argumentos para el servicio en el campo **parámetros de inicio** . Un programa de control de servicios puede iniciar un servicio y especificar sus argumentos con la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .

Cuando se inicia el servicio, el SCM realiza los siguientes pasos:

-   Recuperar la información de la cuenta almacenada en la base de datos.
-   Inicie sesión en la cuenta de servicio.
-   Cargue el perfil de usuario.
-   Cree el servicio en estado suspendido.
-   Asigne el token de inicio de sesión al proceso.
-   Permite que el proceso se ejecute.

 

 



