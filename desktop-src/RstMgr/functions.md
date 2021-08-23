---
title: Funciones del Administrador de reinicio
description: La API de Restart Manager usa las funciones identificadas en la tabla siguiente.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Restart Manager Restart Mgr , reference, functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d628fcd5c1f6488d69152340dd76ae59ac27ea93b2ca157179a052883a26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010203"
---
# <a name="restart-manager-functions"></a>Funciones del Administrador de reinicio

La API de Restart Manager usa las funciones identificadas en la tabla siguiente.



| Función                                           | Descripción                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Modifica las acciones de apagado o reinicio.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Inicia una nueva sesión de Restart Manager.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Une el proceso de una aplicación a una sesión existente de Restart Manager.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Finaliza la sesión del Administrador de reinicio.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registra recursos, como nombres de archivo, nombres cortos de servicio o estructuras [**RM \_ UNIQUE \_ PROCESS,**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) en una sesión de Restart Manager.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Lo usan los instaladores para obtener una lista de todas las aplicaciones afectadas por los recursos registrados y su estado actual.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Consulta el estado de las modificaciones de apagado y reinicio que ya se han aplicado.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Inicia el apagado de aplicaciones y servicios.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Quita las modificaciones de apagado y reinicio que ya se han aplicado.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Reinicia las aplicaciones y servicios que la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ha apagado y que se han registrado para reiniciarse **mediante RegisterApplicationRestart.** |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Cancela la función [**RmGetList,**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) actual.                                                            |



 

 

 




