---
description: Se requiere un cierre adecuado de las sesiones de comunicaciones y de una aplicación completa para evitar que los recursos permanezcan relacionados en las llamadas o aplicaciones que ya no las necesiten.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Apagado de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688410"
---
# <a name="tapi-shutdown"></a>Apagado de TAPI

Se requiere un cierre adecuado de las sesiones de comunicaciones y de una aplicación completa para evitar que los recursos permanezcan relacionados en las llamadas o aplicaciones que ya no las necesiten.

TAPI proporciona una serie de funciones y métodos para ayudar en el proceso. Obviamente, la aplicación también debe asumir la responsabilidad de liberar correctamente la memoria asignada, ya sea en forma de estructuras de datos o de referencias COM.



| Funciones de TAPI 2. x                                                            | Descripción                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Anula el registro de la aplicación como un controlador para llamadas de telefonía asistidas. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Desconecta la aplicación como administrador de llamadas en la línea determinada.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Cierra el uso de la aplicación de la abstracción de línea.            |



 



| Interfaces o métodos TAPI 3. x                                            | Descripción                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Quita cualquier registro de notificación de eventos realizado por la aplicación. |
| [**ITTAPI:: Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Desconecta la aplicación como administrador de llamadas.                             |



 

 

 
