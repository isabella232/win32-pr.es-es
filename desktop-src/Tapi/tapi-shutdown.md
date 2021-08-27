---
description: Se requiere el apagado correcto de las sesiones de comunicaciones y de toda una aplicación para evitar que los recursos que permanecen vinculados a llamadas o aplicaciones que ya no los necesitan.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Apagado de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88303d2475a2ce0a21478575483c0fd93e44e96b71efa83790b7973343d6d9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080445"
---
# <a name="tapi-shutdown"></a>Apagado de TAPI

Se requiere el apagado correcto de las sesiones de comunicaciones y de toda una aplicación para evitar que los recursos que permanecen vinculados a llamadas o aplicaciones que ya no los necesitan.

TAPI proporciona una serie de funciones y métodos para ayudar en el proceso. Obviamente, la aplicación también debe asumir la responsabilidad de liberar correctamente la memoria asignada, ya sea en forma de estructuras de datos o referencias COM.



| Funciones TAPI 2.x                                                            | Descripción                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Anula el registro de la aplicación como controlador para llamadas de telefonía asistidas. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Desconecta la aplicación como administrador para las llamadas en la línea dada.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Cierra el uso de la aplicación de la abstracción de línea.            |



 



| Interfaces o métodos tapi 3.x                                            | Descripción                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Quita los registros de notificaciones de eventos realizados por la aplicación. |
| [**ITTAPI::Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Desconecta la aplicación como administrador de llamadas.                             |



 

 

 
