---
title: Información de autenticación de usuario
description: El servicio Connection Manager acceso remoto en el equipo cliente envía un nombre de usuario y una contraseña al servidor RAS en el equipo remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361965"
---
# <a name="user-authentication-information"></a>Información de autenticación de usuario

El servicio Connection Manager acceso remoto en el equipo cliente envía un nombre de usuario y una contraseña al servidor RAS en el equipo remoto. Antes de establecer una conexión, el servidor remoto usa esta información para autenticar al usuario. De forma predeterminada, el Connection Manager remoto envía el nombre de usuario y la contraseña del usuario que ha iniciado sesión actualmente. El cliente RAS puede usar la [**estructura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) especificada en la llamada a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar un nombre de usuario y una contraseña diferentes.

Si el servidor remoto no puede autenticar al usuario con la información [](paused-states.md) especificada, puede permitir que la operación de conexión entre en un estado en pausa para permitir que el cliente RAS recopile distintos datos de autenticación del usuario.

 

 