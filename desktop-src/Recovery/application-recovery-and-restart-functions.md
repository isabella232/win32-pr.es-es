---
title: Funciones de recuperación y reinicio de aplicaciones
description: Recuperación y reinicio de aplicaciones define las siguientes funciones
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024625"
---
# <a name="application-recovery-and-restart-functions"></a>Funciones de recuperación y reinicio de aplicaciones

Application Recovery y Restart definen las siguientes funciones:



| Función                                                                               | Descripción                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indica que la aplicación que realiza la llamada ha completado su recuperación de datos.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indica que la aplicación que realiza la llamada sigue recuperando datos.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Recupera un puntero a la rutina de devolución de llamada de recuperación registrada para el proceso especificado. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Recupera la información de reinicio registrada para el proceso especificado.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registra la instancia activa de una aplicación para su recuperación.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registra la instancia activa de una aplicación para reiniciarla.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Quita la instancia activa de una aplicación de la lista de recuperación.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Quita la instancia activa de una aplicación de la lista de reinicio.                       |



 

 

 