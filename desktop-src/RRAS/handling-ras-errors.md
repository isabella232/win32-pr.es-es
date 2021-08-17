---
title: Control de errores ras
description: Cuando se produce un error, el Connection Manager remoto invoca el controlador de notificaciones del cliente.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- Ras del servicio de acceso remoto, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b870678eb2dbe95c190bc67415b9abb5481c33918429194404893349c0d7f7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791283"
---
# <a name="handling-ras-errors"></a>Control de errores ras

Cuando se produce un error, el Connection Manager remoto invoca el controlador de notificaciones del cliente. La notificación indica el estado de conexión cuando se produjo el error y un código que identifica el error. En estos casos, el controlador de notificaciones debe llamar [**a RasHangUp para**](/windows/desktop/api/Ras/nf-ras-rashangupa) finalizar la conexión RAS.

Los códigos de error que identifican los errores ras se definen en el archivo raserror.h. El cliente RAS puede usar la [**función RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) para obtener una cadena de presentación que describa el error. Consulte [Códigos de error de enrutamiento y acceso remoto](routing-and-remote-access-error-codes.md) para obtener una descripción de estos errores.

 

 




