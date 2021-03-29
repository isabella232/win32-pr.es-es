---
title: Control de errores de RAS
description: Cuando se produce un error, el administrador de conexiones de acceso remoto invoca el controlador de notificaciones del cliente.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS de servicio de acceso remoto, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778403"
---
# <a name="handling-ras-errors"></a>Control de errores de RAS

Cuando se produce un error, el administrador de conexiones de acceso remoto invoca el controlador de notificaciones del cliente. La notificación indica el estado de conexión cuando se produjo el error y un código que identifica el error. En estos casos, el controlador de notificación debe llamar a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para finalizar la conexión RAS.

Los códigos de error que identifican los errores de RAS se definen en el archivo raserror. h. El cliente RAS puede usar la función [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) para obtener una cadena de presentación que describa el error. Consulte [códigos de error de enrutamiento y acceso remoto](routing-and-remote-access-error-codes.md) para obtener una descripción de estos errores.

 

 




