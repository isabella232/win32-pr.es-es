---
description: Todos los usuarios tienen acceso de lectura a la lista de procesos del sistema y hay una serie de funciones diferentes que enumeran los procesos activos. La función que debe usar dependerá de factores como la compatibilidad con la plataforma deseada.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Enumeración de procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062815"
---
# <a name="process-enumeration"></a>Enumeración de procesos

Todos los usuarios tienen acceso de lectura a la lista de procesos del sistema y hay una serie de funciones diferentes que enumeran los procesos activos. La función que debe usar dependerá de factores como la compatibilidad con la plataforma deseada.

Las funciones siguientes se usan para enumerar los procesos.



| Función                                                    | Descripción                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera el identificador de proceso para cada objeto de proceso del sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera información sobre el primer proceso encontrado en una instantánea del sistema.    |
| [**Process32Siguiente**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera información sobre el siguiente proceso registrado en una instantánea del sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera información sobre los procesos activos en el servidor de terminal especificado. |



 

Las funciones toolhelp y [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumeran todos los procesos. Para enumerar los procesos que se ejecutan en una cuenta de usuario específica, use [**WTSEnumerateProcesses y**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) filtre por el SID del usuario. Puede filtrar por el identificador de sesión para ocultar los procesos que se ejecutan en otras sesiones de terminal Server.

También puede filtrar los procesos por cuenta de usuario, independientemente de la función de enumeración, llamando a [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)y [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con **TokenUser**. Sin embargo, no puede abrir un proceso protegido por un descriptor de seguridad a menos que se le haya concedido acceso.

 

 
