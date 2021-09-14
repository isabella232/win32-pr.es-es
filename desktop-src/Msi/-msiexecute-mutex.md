---
description: MsiExecute Mutex solo se establece mientras se procesa la tabla \_ InstallExecuteSequence, la tabla AdminExecuteSequence o la tabla AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute exclusión mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159303"
---
# <a name="_msiexecute-mutex"></a>\_MSIExecute Mutex

MsiExecute Mutex solo se establece mientras se procesa la tabla \_ [InstallExecuteSequence,](installexecutesequence-table.md)la tabla [AdminExecuteSequence](adminexecutesequence-table.md)o la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).

Dado que dos instalaciones no se pueden ejecutar en el mismo proceso, un intento de llamar a la interfaz de programación de aplicaciones (API) del instalador devuelve ERROR \_ INSTALL \_ ALREADY RUNNING \_ (1618) en dos casos:

-   Mientras se \_ establece MSIExecute Mutex.
-   Mientras el proceso actual está procesando [la tabla InstallUISequence](installuisequence-table.md) o [la tabla AdminUISequence](adminuisequence-table.md).

Consulte los [mensajes de registro de](event-logging.md) eventos para obtener información sobre la aplicación que se está instalando.

En los casos en los que no es práctico devolver un error ERROR INSTALL ALREADY RUNNING, puede recuperar el estado actual del servicio instalador de Windows antes de intentar iniciar la instalación mediante la función \_ \_ \_ [**QueryServiceStatusEx.**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) El Windows installer está en ejecución actualmente si el valor del miembro **dwControlsAccepted** de la estructura [**SERVICE STATUS \_ \_ PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) devuelta es **SERVICE ACCEPT \_ \_ SHUTDOWN**.

**Windows Installer 2.0:** No se admite. El uso de la [**función QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) para recuperar el estado actual del servicio instalador de Windows requiere Windows Installer versión 3.0 o posterior.

 

 
