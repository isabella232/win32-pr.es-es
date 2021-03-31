---
title: Información de autenticación de usuario
description: El servicio Administrador de conexiones de acceso remoto en el equipo cliente envía un nombre de usuario y una contraseña al servidor RAS del equipo remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904641"
---
# <a name="user-authentication-information"></a>Información de autenticación de usuario

El servicio Administrador de conexiones de acceso remoto en el equipo cliente envía un nombre de usuario y una contraseña al servidor RAS del equipo remoto. Antes de establecer una conexión, el servidor remoto utiliza esta información para autenticar al usuario. De forma predeterminada, el administrador de conexiones de acceso remoto envía el nombre de usuario y la contraseña del usuario que ha iniciado sesión actualmente. El cliente RAS puede usar la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) especificada en la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar un nombre de usuario y una contraseña diferentes.

Si el servidor remoto no puede autenticar al usuario con la información especificada, puede permitir que la operación de conexión entre en un [Estado de pausa](paused-states.md) para permitir que el cliente ras recopile datos de autenticación diferentes del usuario.

 

 