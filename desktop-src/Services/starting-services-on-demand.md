---
description: El usuario puede iniciar un servicio con la utilidad del panel de control Servicios. El usuario puede especificar argumentos para el servicio en el campo Parámetros de inicio. Un programa de control de servicio puede iniciar un servicio y especificar sus argumentos con la función StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Iniciar servicios a petición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170790"
---
# <a name="starting-services-on-demand"></a>Iniciar servicios a petición

El usuario puede iniciar un servicio con la utilidad del panel de control Servicios. El usuario puede especificar argumentos para el servicio en el **campo Parámetros de** inicio. Un programa de control de servicio puede iniciar un servicio y especificar sus argumentos con la [**función StartService.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)

Cuando se inicia el servicio, el SCM realiza los pasos siguientes:

-   Recupere la información de la cuenta almacenada en la base de datos.
-   Inicie sesión en la cuenta de servicio.
-   Cargue el perfil de usuario.
-   Cree el servicio en estado suspendido.
-   Asigne el token de inicio de sesión al proceso.
-   Permita que se ejecute el proceso.

 

 



