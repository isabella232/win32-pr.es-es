---
title: Funciones de recuperación y reinicio de aplicaciones
description: 'Recuperación y reinicio de aplicaciones define las siguientes funciones:'
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149471"
---
# <a name="application-recovery-and-restart-functions"></a>Funciones de recuperación y reinicio de aplicaciones

Recuperación y reinicio de aplicaciones define las siguientes funciones:



| Función                                                                               | Descripción                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indica que la aplicación que realiza la llamada ha completado su recuperación de datos.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indica que la aplicación que realiza la llamada está continuando recuperando datos.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Recupera un puntero a la rutina de devolución de llamada de recuperación registrada para el proceso especificado. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Recupera la información de reinicio registrada para el proceso especificado.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registra la instancia activa de una aplicación para la recuperación.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registra la instancia activa de una aplicación para que se reinicie.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Quita la instancia activa de una aplicación de la lista de recuperación.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Quita la instancia activa de una aplicación de la lista de reinicio.                       |



 

 

 